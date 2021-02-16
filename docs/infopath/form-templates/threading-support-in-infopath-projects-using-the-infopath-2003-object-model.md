---
title: Suporte a threading em projetos do InfoPath usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- multithread modelos de formulário compatível com o 2003 infopath [infopath 2007], threading [InfoPath 2007] suportam projetos usando modelos de formulário do InfoPath 2003 compatível, suporte a segmentação de modelo de objeto do InfoPath 2003
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Os objetos COM são acessados por meio de montagens com interoperabilidade instaladas Microsoft.Office.Interop.InfoPath.dll Microsoft.Office.Interop.InfoPath.SemiTrust.dll e Microsoft.Office.Interop.InfoPath.Xml.dll. O Microsoft InfoPath não dá suporte a chamadas feitas em vários threads. Isso inclui interfaces para objetos para Microsoft XML Core Services (MSXML) que são envoltas pelo namespace Microsoft.Office.Interop.InfoPath.SemiTrust (a maioria deles possui o prefixo IXMLDOM) e todas as interfaces são expostas pelo namespace Microsoft.Office.Interop.InfoPath.Xml, nenhum deles são threads seguros.
ms.openlocfilehash: ca00593eebe17586c4f77b4b91adc158c4f649fd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537840"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>Suporte a threading em projetos do InfoPath usando o modelo de objeto do InfoPath 2003

Os objetos COM são acessados por meio de montagens com interoperabilidade instaladas Microsoft.Office.Interop.InfoPath.dll Microsoft.Office.Interop.InfoPath.SemiTrust.dll e Microsoft.Office.Interop.InfoPath.Xml.dll. O Microsoft InfoPath não dá suporte a chamadas feitas em vários threads. Isso inclui interfaces para objetos de serviços de básicos de Isso inclui interfaces para objetos para Microsoft XML Core Services (MSXML) que são envoltas pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** (a maioria deles possui o prefixo IXMLDOM) e todas as interfaces são expostas pelo namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) nenhum deles são threads seguros. 
  
Todas as chamadas realizadas para esses objetos COM devem ser emitidas em uma única conversa. O código gerenciado em um projeto InfoPath pode criar outros threads para realizar o trabalho de tela de fundo, mas códigos rodando em threads diferentes de conversa principal não podem acionar os modelos de objeto do InfoPath.
  
Se seu projeto de código gerenciado InfoPath usa vários threads, tenha cuidado ao compartilhar objetos entre threads.  Nenuma referências ao Modelo de Objeto do Documento XML (DOM Document) ou referências a InfoPath objetos deverão ser compartilhadas entre threads. 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>Fazendo chamadas assíncronas para o modelo de objeto do InfoPath

Para situações em que é necessário ligar para um processo como um temporizador em execução em um thread separado, é possível contornar o fato de que o modelo de objeto do InfoPath não dá suporte a esses chamadas. 
  
O exemplo a seguir cria uma instância **System.Timers.Timer** no método Startup de formulário e fixa um retorno de chamada assíncrono para o cronômetro. Além disso, uma instância do formulário de janela invisível (**Form**) é criado. Quando o tempo decorrido da função retorno executa um por segundo, chamadas na Win32 função **PostMessage** para postar uma mensagem para a janela invisível. A janela invisível tem a função **WndProc** que processa a mensagem, ela recebe essa mensagem da função de retorno de chamada de temporizador e atualiza o modelo de objeto de documento (DOM) XML do formulário. Instale este formulário como um formulário confiável para executar. Confira informações sobre depuração de um modelo de formulário totalmente confiáveis [visualização e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md). Confira informações sobre a implantação de um modelo de formulário totalmente confiáveis [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```



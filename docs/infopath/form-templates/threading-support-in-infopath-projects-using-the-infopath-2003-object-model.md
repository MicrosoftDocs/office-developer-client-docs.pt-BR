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
ms.openlocfilehash: 1be2bd0181c47097440af54f1aa804a4f17b30bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299836"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a><span data-ttu-id="cb6d0-105">Suporte a threading em projetos do InfoPath usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="cb6d0-105">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="cb6d0-106">Os objetos COM são acessados por meio de montagens com interoperabilidade instaladas Microsoft.Office.Interop.InfoPath.dll Microsoft.Office.Interop.InfoPath.SemiTrust.dll e Microsoft.Office.Interop.InfoPath.Xml.dll. O Microsoft InfoPath não dá suporte a chamadas feitas em vários threads.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-106">The COM objects accessed through the Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll, and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies installed by Microsoft InfoPath do not support calls made on multiple threads.</span></span> <span data-ttu-id="cb6d0-107">Isso inclui interfaces para objetos de serviços de básicos de Isso inclui interfaces para objetos para Microsoft XML Core Services (MSXML) que são envoltas pelo namespace **Microsoft.Office.Interop.InfoPath.SemiTrust** (a maioria deles possui o prefixo IXMLDOM) e todas as interfaces são expostas pelo namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) nenhum deles são threads seguros.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-107">This includes the interfaces for Microsoft XML Core Services (MSXML) objects that are wrapped by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace (most of which have names that are prefixed with IXMLDOM) and all of the interfaces exposed by the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml)  namespace, none of which are thread-safe.</span></span> 
  
<span data-ttu-id="cb6d0-108">Todas as chamadas realizadas para esses objetos COM devem ser emitidas em uma única conversa.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-108">All calls made to these COM objects must be issued on a single thread.</span></span> <span data-ttu-id="cb6d0-109">O código gerenciado em um projeto InfoPath pode criar outros threads para realizar o trabalho de tela de fundo, mas códigos rodando em threads diferentes de conversa principal não podem acionar os modelos de objeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-109">Managed code in an InfoPath project can create other threads to perform background work, but code running on threads other than the main thread cannot call into the InfoPath object models.</span></span>
  
<span data-ttu-id="cb6d0-110">Se seu projeto de código gerenciado InfoPath usa vários threads, tenha cuidado ao compartilhar objetos entre threads. </span><span class="sxs-lookup"><span data-stu-id="cb6d0-110">If your InfoPath managed code project uses multiple threads, you must be careful about sharing objects between threads.</span></span> <span data-ttu-id="cb6d0-111">Nenuma referências ao Modelo de Objeto do Documento XML (DOM Document) ou referências a InfoPath objetos deverão ser compartilhadas entre threads.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-111">No references to the XML Document Object Model (DOM) or references to InfoPath objects should be shared between threads.</span></span> 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a><span data-ttu-id="cb6d0-112">Fazendo chamadas assíncronas para o modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="cb6d0-112">Making Asynchronous Calls to the InfoPath Object Model</span></span>

<span data-ttu-id="cb6d0-113">Para situações em que é necessário ligar para um processo como um temporizador em execução em um thread separado, é possível contornar o fato de que o modelo de objeto do InfoPath não dá suporte a esses chamadas.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-113">For situations where it is necessary to call into a process such as a timer running on a separate thread, it is possible to work around the fact that the InfoPath object model does not support such calls.</span></span> 
  
<span data-ttu-id="cb6d0-114">O exemplo a seguir cria uma instância **System.Timers.Timer** no método Startup de formulário e fixa um retorno de chamada assíncrono para o cronômetro.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-114">The following example creates a **System.Timers.Timer** instance in the _Startup method of the form and hooks up an asynchronous callback to the timer.</span></span> <span data-ttu-id="cb6d0-115">Além disso, uma instância do formulário de janela invisível (**Form**) é criado.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-115">In addition, an invisible instance of the window form (**System.Windows.Forms.Form**) is created.</span></span> <span data-ttu-id="cb6d0-116">Quando o tempo decorrido da função retorno executa um por segundo, chamadas na Win32 função**PostMessage** para postar uma mensagem para a janela invisível.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-116">When the timer elapsed callback function executes once per second, it calls into the Win32 **PostMessage** function to post a message to the invisible window.</span></span> <span data-ttu-id="cb6d0-117">A janela invisível tem a função **WndProc** que processa a mensagem, ela recebe essa mensagem da função de retorno de chamada de temporizador e atualiza o modelo de objeto de documento (DOM) XML do formulário.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-117">The invisible window has a **WndProc** function that processes the message it receives from the timer callback function, and updates the XML document object model (DOM) of the form.</span></span> <span data-ttu-id="cb6d0-118">Instale este formulário como um formulário confiável para executar.</span><span class="sxs-lookup"><span data-stu-id="cb6d0-118">This form must be installed as a fully trusted form to run.</span></span> <span data-ttu-id="cb6d0-119">Confira informações sobre depuração de um modelo de formulário totalmente confiáveis [visualização e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="cb6d0-119">For information on debugging a fully trusted form template, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> <span data-ttu-id="cb6d0-120">Confira informações sobre a implantação de um modelo de formulário totalmente confiáveis [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="cb6d0-120">For information on deploying a fully trusted form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
  
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
    [InfoPathNamespace("xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
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



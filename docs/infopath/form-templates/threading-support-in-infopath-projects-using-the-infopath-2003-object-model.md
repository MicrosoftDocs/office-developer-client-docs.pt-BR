---
title: Suporte a threading em projetos do InfoPath usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Multithreading modelos de formulário compatíveis 2003 infopath [infopath 2007], threading [InfoPath 2007], suportam para projetos usando o modelo de objeto do InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, suporte a segmentação
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Os objetos COM acessada por meio de assemblies de interoperabilidade Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll e Microsoft.Office.Interop.InfoPath.Xml.dll instalados pelo Microsoft InfoPath não oferecem suporte a chamadas feita em vários threads. Isso inclui as interfaces para objetos do Microsoft XML Core Services (MSXML) que devem ser quebradas por namespace SemiTrust (a maioria dos quais têm nomes que são prefixados com IXMLDOM) e todas as interfaces expostas pela Namespace Microsoft.Office.Interop.InfoPath.Xml, sendo que nenhum deles são thread-safe.
ms.openlocfilehash: 314ef57e11295c0b2dbc9866c5faa392aab055ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765704"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a><span data-ttu-id="f1c79-105">Suporte a threading em projetos do InfoPath usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f1c79-105">Threading Support in InfoPath Projects Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="f1c79-106">Os objetos COM acessada por meio de assemblies de interoperabilidade Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll e Microsoft.Office.Interop.InfoPath.Xml.dll instalados pelo Microsoft InfoPath não oferecem suporte a chamadas feita em vários threads.</span><span class="sxs-lookup"><span data-stu-id="f1c79-106">The COM objects accessed through the Microsoft.Office.Interop.InfoPath.dll, Microsoft.Office.Interop.InfoPath.SemiTrust.dll, and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies installed by Microsoft InfoPath do not support calls made on multiple threads.</span></span> <span data-ttu-id="f1c79-107">Isso inclui as interfaces para objetos do Microsoft XML Core Services (MSXML) que devem ser quebradas por namespace **SemiTrust** (a maioria dos quais têm nomes que são prefixados com IXMLDOM) e todas as interfaces expostas pelo o namespace [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , sendo que nenhum deles são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f1c79-107">This includes the interfaces for Microsoft XML Core Services (MSXML) objects that are wrapped by the **Microsoft.Office.Interop.InfoPath.SemiTrust** namespace (most of which have names that are prefixed with IXMLDOM) and all of the interfaces exposed by the [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml)  namespace, none of which are thread-safe.</span></span> 
  
<span data-ttu-id="f1c79-108">Todas as chamadas feitas para esses objetos COM devem ser emitidas em um único segmento.</span><span class="sxs-lookup"><span data-stu-id="f1c79-108">All calls made to these COM objects must be issued on a single thread.</span></span> <span data-ttu-id="f1c79-109">Código gerenciado em um InfoPath projeto pode criar outros segmentos para executar o trabalho de plano de fundo, mas o código em execução em segmentos que não seja o segmento principal não é possível chamar em modelos de objeto do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f1c79-109">Managed code in an InfoPath project can create other threads to perform background work, but code running on threads other than the main thread cannot call into the InfoPath object models.</span></span>
  
<span data-ttu-id="f1c79-110">Se seu projeto de código gerenciado do InfoPath usa vários threads, você deve tomar cuidado sobre o compartilhamento de objetos entre threads.</span><span class="sxs-lookup"><span data-stu-id="f1c79-110">If your InfoPath managed code project uses multiple threads, you must be careful about sharing objects between threads.</span></span> <span data-ttu-id="f1c79-111">Nenhuma referência para o XML DOM Document Object Model () ou referências aos objetos do InfoPath devem ser compartilhadas entre os threads.</span><span class="sxs-lookup"><span data-stu-id="f1c79-111">No references to the XML Document Object Model (DOM) or references to InfoPath objects should be shared between threads.</span></span> 
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a><span data-ttu-id="f1c79-112">Fazendo chamadas assíncronas ao modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="f1c79-112">Making Asynchronous Calls to the InfoPath Object Model</span></span>

<span data-ttu-id="f1c79-113">Para situações em que é necessário ligar para um processo como um cronômetro em execução em um segmento separado, é possível contornar o fato de que o modelo de objeto do InfoPath não oferece suporte a essas chamadas.</span><span class="sxs-lookup"><span data-stu-id="f1c79-113">For situations where it is necessary to call into a process such as a timer running on a separate thread, it is possible to work around the fact that the InfoPath object model does not support such calls.</span></span> 
  
<span data-ttu-id="f1c79-114">O exemplo a seguir cria uma instância de **System.Timers.Timer** no método Startup do formulário e conecta um retorno de chamada assíncrono para o timer.</span><span class="sxs-lookup"><span data-stu-id="f1c79-114">The following example creates a **System.Timers.Timer** instance in the _Startup method of the form and hooks up an asynchronous callback to the timer.</span></span> <span data-ttu-id="f1c79-115">Além disso, uma instância invisível do formulário janela (**Form**) é criada.</span><span class="sxs-lookup"><span data-stu-id="f1c79-115">In addition, an invisible instance of the window form (**System.Windows.Forms.Form**) is created.</span></span> <span data-ttu-id="f1c79-116">Quando o cronômetro decorrido a função de retorno de chamada executa uma vez por segundo, ela chama a função Win32 **PostMessage** postar uma mensagem na janela invisível.</span><span class="sxs-lookup"><span data-stu-id="f1c79-116">When the timer elapsed callback function executes once per second, it calls into the Win32 **PostMessage** function to post a message to the invisible window.</span></span> <span data-ttu-id="f1c79-117">A janela invisível tem uma função de **WndProc** que processa a mensagem, ele recebe a partir da função de retorno de chamada de timer e atualiza o modelo de objeto de documento (DOM) XML do formulário.</span><span class="sxs-lookup"><span data-stu-id="f1c79-117">The invisible window has a **WndProc** function that processes the message it receives from the timer callback function, and updates the XML document object model (DOM) of the form.</span></span> <span data-ttu-id="f1c79-118">Este formulário deve ser instalado como um formulário totalmente confiável seja executado.</span><span class="sxs-lookup"><span data-stu-id="f1c79-118">This form must be installed as a fully trusted form to run.</span></span> <span data-ttu-id="f1c79-119">Para obter informações sobre a depuração de um modelo de formulário totalmente confiável, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="f1c79-119">For information on debugging a fully trusted form template, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> <span data-ttu-id="f1c79-120">Para obter informações sobre como implantar um modelo de formulário totalmente confiável, consulte [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="f1c79-120">For information on deploying a fully trusted form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
  
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



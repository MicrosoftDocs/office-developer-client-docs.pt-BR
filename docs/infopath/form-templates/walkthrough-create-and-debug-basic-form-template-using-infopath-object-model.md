---
title: 'Passo a passo: criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- modelos de formulário [InfoPath 2007], passo a passo, modelos de formulário [InfoPath 2007], criação de modelos de formulário compatíveis com o InfoPath 2003, o InfoPath 2003
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Este tópico fornece um passo a passo para criar um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace Microsoft. Office. Interop. InfoPath. SemiTrust.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414337"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="946a7-104">Passo a passo: criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="946a7-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="946a7-105">Este tópico fornece um passo a passo para criar um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto compatível com o InfoPath 2003 fornecido pelo namespace [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="946a7-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="946a7-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="946a7-106">Hello World</span></span>

<span data-ttu-id="946a7-107">No exemplo a seguir, você aprenderá como exibir uma caixa de diálogo alerta simples usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do modelo de objeto compatível com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="946a7-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="946a7-108">Criar um novo modelo de formulário do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="946a7-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="946a7-109">Crie um novo modelo de formulário que funcione com o modelo de objeto compatível com o InfoPath 2003, conforme descrito em [criar um modelo de formulário usando o modelo de objeto do infopath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="946a7-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="946a7-110">Nomeie o projeto de modelo de formulário HelloWorld e salve-o.</span><span class="sxs-lookup"><span data-stu-id="946a7-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="946a7-111">O sistema do projeto cria arquivos de código e de projeto e, em seguida, abre um modelo de formulário em branco no modo de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="946a7-111">The project system creates code and project files, and then opens a blank form template in InfoPath design mode.</span></span> <span data-ttu-id="946a7-112">Agora você está pronto para adicionar manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="946a7-112">You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="946a7-113">Adicionar um botão com um manipulador de eventos OnClick</span><span class="sxs-lookup"><span data-stu-id="946a7-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="946a7-114">Na seção **controles** da guia **página inicial** , clique no controle **botão** para inseri-lo no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="946a7-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="946a7-115">Clique com o botão direito do mouse no controle e clique em **Propriedades do botão**.</span><span class="sxs-lookup"><span data-stu-id="946a7-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="946a7-116">Altere o **rótulo** para alerta.</span><span class="sxs-lookup"><span data-stu-id="946a7-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="946a7-117">Altere a **ID** para Alertid.</span><span class="sxs-lookup"><span data-stu-id="946a7-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="946a7-118">Clique em **Editar código de formulário**.</span><span class="sxs-lookup"><span data-stu-id="946a7-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="946a7-119">Um esqueleto de manipulador de eventos [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) para o evento onclick é criado e o foco é movido para o editor de código no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="946a7-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="946a7-120">Para obter mais informações sobre como trabalhar com manipuladores de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="946a7-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="946a7-121">Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.</span><span class="sxs-lookup"><span data-stu-id="946a7-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="946a7-122">Adicionar código de formulário ao manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="946a7-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="946a7-123">No manipulador \*\*\*\* de eventos OnClick, digite o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="946a7-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="946a7-124">Observe que uma lista suspensa do Microsoft IntelliSense é exibida após você digitar cada período na linha de código.</span><span class="sxs-lookup"><span data-stu-id="946a7-124">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code.</span></span> <span data-ttu-id="946a7-125">O manipulador de eventos inteiro deve se parecer com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="946a7-125">The entire event handler should look like the following:</span></span>
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > <span data-ttu-id="946a7-126">Como alternativa ao uso do método **Alert** , você pode usar o método **MessageBox. show** do namespace **System. Windows. Forms** para exibir uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="946a7-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="946a7-127">Para fazer isso, você deve adicionar uma referência ao assembly System. Windows. Forms, adicionar `using System.Windows.Forms;` ou `Imports System.Windows.Forms` às diretivas no início do seu arquivo de código e, em seguida, digitar uma linha de código como a seguinte:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="946a7-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="946a7-128">Alterne para a janela modo de design do InfoPath e, em seguida, clique no botão **Visualizar** na guia **página inicial** .</span><span class="sxs-lookup"><span data-stu-id="946a7-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="946a7-129">Na janela de **Visualização** , clique no botão **alerta** .</span><span class="sxs-lookup"><span data-stu-id="946a7-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="946a7-130">Será exibida uma caixa de mensagem com o texto "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="946a7-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="946a7-131">O procedimento a seguir mostra como adicionar pontos de interrupção de depuração ao seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="946a7-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="946a7-132">Depurar código de formulário</span><span class="sxs-lookup"><span data-stu-id="946a7-132">Debug form code</span></span>

1. <span data-ttu-id="946a7-133">No editor de código, clique na barra cinza à esquerda da linha:</span><span class="sxs-lookup"><span data-stu-id="946a7-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="946a7-134">Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="946a7-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="946a7-135">No menu **Depurar**, clique em **Iniciar Depuração** (ou pressione F5).</span><span class="sxs-lookup"><span data-stu-id="946a7-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="946a7-136">Na janela de **Visualização** do InfoPath, clique no botão **alerta** .</span><span class="sxs-lookup"><span data-stu-id="946a7-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="946a7-137">O editor de código recebe o foco e a linha do ponto de interrupção é realçada.</span><span class="sxs-lookup"><span data-stu-id="946a7-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="946a7-138">No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código.</span><span class="sxs-lookup"><span data-stu-id="946a7-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="946a7-139">O código do método **Alert** é executado e o "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="946a7-139">The **Alert** method code is executed, and the "Hello World!"</span></span> <span data-ttu-id="946a7-140">o alerta é exibido na janela de **Visualização** do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="946a7-140">alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="946a7-141">Obtendo o nome do usuário atual</span><span class="sxs-lookup"><span data-stu-id="946a7-141">Getting the Current User's Name</span></span>

<span data-ttu-id="946a7-142">Usando as classes do .NET Framework, você pode obter acesso a funcionalidades que não estavam disponíveis no script.</span><span class="sxs-lookup"><span data-stu-id="946a7-142">By using the .NET Framework classes, you can get access to functionality that was not easily available in script.</span></span> <span data-ttu-id="946a7-143">Neste exemplo, você aprenderá como usar as classes do .NET Framework para recuperar o nome do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="946a7-143">In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="946a7-144">Adicionar um manipulador de eventos OnLoad</span><span class="sxs-lookup"><span data-stu-id="946a7-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="946a7-145">Abra o projeto do InfoPath HelloWorld que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="946a7-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="946a7-146">Na guia **Exibir** , clique em **Mostrar campos**.</span><span class="sxs-lookup"><span data-stu-id="946a7-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="946a7-147">Clique com o botão \*\*\*\* direito do mouse no nó myFields e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="946a7-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="946a7-148">Em **nome**, digite **funcionário**e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="946a7-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="946a7-149">Arraste o nó **Employee** para o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="946a7-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="946a7-150">Na guia **desenvolvedor** , clique **em carregar evento**.</span><span class="sxs-lookup"><span data-stu-id="946a7-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="946a7-151">Isso criará um manipulador de eventos para o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) e o foco será movido para o editor de código.</span><span class="sxs-lookup"><span data-stu-id="946a7-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="946a7-152">O código neste manipulador de eventos será chamado cada vez que o formulário for carregado.</span><span class="sxs-lookup"><span data-stu-id="946a7-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="946a7-153">O procedimento a seguir mostra como adicionar o código de formulário que recupera o nome do usuário para o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="946a7-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="946a7-154">Adicionar código de formulário</span><span class="sxs-lookup"><span data-stu-id="946a7-154">Add form code</span></span>

1. <span data-ttu-id="946a7-155">No manipulador de eventos **OnLoad** , digite o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="946a7-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. <span data-ttu-id="946a7-156">Compilar e visualizar o formulário.</span><span class="sxs-lookup"><span data-stu-id="946a7-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="946a7-157">A caixa de texto do funcionário agora deve ser preenchida com seu nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="946a7-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="946a7-158">Para obter informações sobre como implantar um modelo de formulário de código gerenciado, consulte [implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="946a7-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="946a7-159">Para obter informações sobre o modelo de objeto do InfoPath e tarefas comuns de programação em modelos de formulário de código gerenciado que funcionam com o modelo de objeto compatível com o InfoPath 2003, consulte underStanding [The infopath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="946a7-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="946a7-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="946a7-160">See also</span></span>

- [<span data-ttu-id="946a7-161">Inicialização e limpeza de códigos que usam o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="946a7-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="946a7-162">Modelos de objeto compatíveis com o InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="946a7-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="946a7-163">Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="946a7-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)


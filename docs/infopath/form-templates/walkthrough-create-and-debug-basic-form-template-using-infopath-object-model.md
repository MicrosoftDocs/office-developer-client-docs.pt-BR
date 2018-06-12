---
title: 'Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], passo a passo, modelos [InfoPath 2007], criando compatíveis com o InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, passo a passo de formulário
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Este tópico fornece um passo a passo de criação de um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace SemiTrust.
ms.openlocfilehash: 3939cfcfdf2a8683fe614c5f49cc8b2719484ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765711"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="f7dc8-104">Passo a passo: Criar e depurar um modelo de formulário básico usando o modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="f7dc8-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="f7dc8-105">Este tópico fornece um passo a passo de criação de um modelo de formulário de código gerenciado do InfoPath básico que funciona com o modelo de objeto do InfoPath 2003 compatíveis fornecido pelo namespace [SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f7dc8-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="f7dc8-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="f7dc8-106">Hello World</span></span>

<span data-ttu-id="f7dc8-107">O exemplo a seguir, você aprenderá como exibir uma caixa de diálogo alerta simples usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) do modelo de objeto compatível com o InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="f7dc8-108">Criar um novo modelo de formulário do InfoPath que funciona com o modelo de objeto compatível com o InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f7dc8-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="f7dc8-109">Crie um novo modelo de formulário que funciona com o modelo de objeto do InfoPath 2003 compatíveis, conforme descrito em [criar um formulário modelo usando o modelo de objeto do InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="f7dc8-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="f7dc8-110">Nome do projeto de modelo de formulário HelloWorld e salvá-lo.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="f7dc8-111">O sistema de projeto cria arquivos de projeto e de código e, depois, abre um modelo de formulário em branco no modo de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-111">The project system creates code and project files, and then opens a blank form template in InfoPath design mode.</span></span> <span data-ttu-id="f7dc8-112">Agora você está pronto para adicionar manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-112">You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="f7dc8-113">Adicionar um botão com um manipulador de eventos OnClick</span><span class="sxs-lookup"><span data-stu-id="f7dc8-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="f7dc8-114">Na seção de **controles** na guia **página inicial** , clique no controle de **botão** para inseri-lo no modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="f7dc8-115">Com o botão direito no controle e, em seguida, clique em **Propriedades do botão**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="f7dc8-116">Altere o **rótulo** para o alerta.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="f7dc8-117">Altere a **ID** para AlertID.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="f7dc8-118">Clique em **Editar o código do formulário**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="f7dc8-119">Um esqueleto de manipulador de evento para o evento [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) é criado e o foco é movido para o editor de código no Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="f7dc8-120">Para obter mais informações sobre como trabalhar com manipuladores de eventos, consulte [Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="f7dc8-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="f7dc8-121">Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="f7dc8-122">Adicione o código de formulário para o manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="f7dc8-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="f7dc8-123">No manipulador de eventos **OnClick** , digite o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="f7dc8-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="f7dc8-124">Observe que é exibida uma lista de lista suspensa do Microsoft IntelliSense após digitar cada período em que a linha de código.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-124">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code.</span></span> <span data-ttu-id="f7dc8-125">O manipulador de eventos inteira deve se parecer com o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7dc8-125">The entire event handler should look like the following:</span></span>
    
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
   > <span data-ttu-id="f7dc8-126">Como alternativa para o uso do método de **alerta** , você pode usar o método **MessageBox. show** do namespace **System.Windows.Forms** para exibir uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="f7dc8-127">Para isso, você deve adicionar uma referência para o assembly System.Windows.Forms, adicionar `using System.Windows.Forms;` ou `Imports System.Windows.Forms` às diretivas no início do seu arquivo de código e digite uma linha de código como o seguinte:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="f7dc8-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="f7dc8-128">Alternar para a janela do modo de design do InfoPath e, em seguida, clique no botão **Visualizar** na guia **página inicial** .</span><span class="sxs-lookup"><span data-stu-id="f7dc8-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="f7dc8-129">Na janela de **visualização** , clique no botão de **alerta** .</span><span class="sxs-lookup"><span data-stu-id="f7dc8-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="f7dc8-130">Será exibida uma caixa de mensagem com o texto "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="f7dc8-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="f7dc8-131">O procedimento a seguir mostra como adicionar pontos de interrupção de depuração ao seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="f7dc8-132">Depurar código de formulário</span><span class="sxs-lookup"><span data-stu-id="f7dc8-132">Debug form code</span></span>

1. <span data-ttu-id="f7dc8-133">No editor de código, clique na barra cinza à esquerda da linha:</span><span class="sxs-lookup"><span data-stu-id="f7dc8-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="f7dc8-134">Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="f7dc8-135">No menu **Depurar**, clique em **Iniciar Depuração** (ou pressione F5).</span><span class="sxs-lookup"><span data-stu-id="f7dc8-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="f7dc8-136">Na janela de **visualização** do InfoPath, clique no botão de **alerta** .</span><span class="sxs-lookup"><span data-stu-id="f7dc8-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="f7dc8-137">O editor de código recebe o foco e a linha de ponto de interrupção é realçada.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="f7dc8-138">No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="f7dc8-139">O código de método de **alerta** é executado e "Olá mundo!"</span><span class="sxs-lookup"><span data-stu-id="f7dc8-139">The **Alert** method code is executed, and the "Hello World!"</span></span> <span data-ttu-id="f7dc8-140">alerta é exibida na janela de **visualização** do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-140">alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="f7dc8-141">Obtendo o nome do usuário atual</span><span class="sxs-lookup"><span data-stu-id="f7dc8-141">Getting the Current User's Name</span></span>

<span data-ttu-id="f7dc8-142">Usando as classes do .NET Framework, você pode obter acesso à funcionalidade que não estava disponível facilmente no script.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-142">By using the .NET Framework classes, you can get access to functionality that was not easily available in script.</span></span> <span data-ttu-id="f7dc8-143">Neste exemplo, você vai aprender como usar as classes do .NET Framework para recuperar o nome do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-143">In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="f7dc8-144">Adicionar um manipulador de eventos OnLoad</span><span class="sxs-lookup"><span data-stu-id="f7dc8-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="f7dc8-145">Abra o projeto do InfoPath HelloWorld que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="f7dc8-146">Na guia **Exibir** , clique em **Mostrar campos**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="f7dc8-147">Com o botão direito no nó **myFields** e, em seguida, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="f7dc8-148">Em **nome**, tipo de **funcionário**, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="f7dc8-149">Arraste o nó do **funcionário** para o modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="f7dc8-150">Na guia **desenvolvedor** , clique **Em evento OnLoad**.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="f7dc8-151">Isso irá criar um manipulador de eventos para o evento [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) , e o foco é movido para o editor de código.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="f7dc8-152">O código no manipulador de eventos será chamado sempre que o formulário é carregado.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="f7dc8-153">O próximo procedimento mostra como adicionar o código de formulário que recupera o nome do usuário para o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="f7dc8-154">Adicione o código de formulário</span><span class="sxs-lookup"><span data-stu-id="f7dc8-154">Add form code</span></span>

1. <span data-ttu-id="f7dc8-155">No manipulador de eventos **OnLoad** , digite o código a seguir:</span><span class="sxs-lookup"><span data-stu-id="f7dc8-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
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

2. <span data-ttu-id="f7dc8-156">Compilar e visualize o formulário.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="f7dc8-157">A caixa de texto de funcionário agora deve ser preenchida com seu nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="f7dc8-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="f7dc8-158">Para obter informações sobre como implantar um modelo de formulário de código gerenciado, consulte [Implantar modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="f7dc8-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="f7dc8-159">Para obter informações sobre o modelo de objeto do InfoPath e tarefas de programação comuns nos modelos de formulário de código gerenciado que funcionam com o modelo de objeto do InfoPath 2003 compatíveis, consulte [Compreendendo o modelo de objeto do InfoPath 2003](understanding-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="f7dc8-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7dc8-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7dc8-160">See also</span></span>

- [<span data-ttu-id="f7dc8-161">Código de inicialização e a limpeza usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f7dc8-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="f7dc8-162">Modelos de objeto do InfoPath 2003 compatíveis</span><span class="sxs-lookup"><span data-stu-id="f7dc8-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="f7dc8-163">Adicionar um manipulador de eventos usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f7dc8-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)


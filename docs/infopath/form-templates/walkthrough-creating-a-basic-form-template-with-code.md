---
title: 'Passo a passo: criar um modelo de formulário básico com código'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- modelos de formulário do [InfoPath 2007], criar código gerenciado, modelos de formulário de código gerenciado do [InfoPath 2007], criação, modelos de formulário [InfoPath 2007], passo a passo, InfoPath 2007, passo a passo
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: No Microsoft InfoPath, você pode escrever lógica de negócios no Visual Basic ou no C# abrindo um modelo de formulário no designer do InfoPath e então usando um dos comandos da interface do usuário para adicionar um manipulador de eventos, que abrirá o ambiente de desenvolvimento do Visual Studio 2012 para que seu código seja escrito.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765729"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="5e724-104">Passo a passo: criar um modelo de formulário básico com código</span><span class="sxs-lookup"><span data-stu-id="5e724-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="5e724-p101">No Microsoft InfoPath, você pode escrever lógica de negócios no Visual Basic ou no C# abrindo um modelo de formulário no designer do InfoPath e então usando um dos comandos da interface do usuário para adicionar um manipulador de eventos, que abrirá o ambiente de desenvolvimento do Visual Studio 2012 para que seu código seja escrito. Por padrão, projetos de modelo de formulário criados usando o Visual Studio 2012 funcionam no modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e724-p101">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code. By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="5e724-p102">Primeiro, este passo a passo mostra como criar um aplicativo Hello World simples usando C# ou Visual Basic no ambiente de desenvolvimento do Visual Studio 2012. O passo a passo conclui com um exemplo de código que mostra como usar a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar o nome do usuário atual e preencher um controle **Caixa de Texto** com esse valor.</span><span class="sxs-lookup"><span data-stu-id="5e724-p102">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment. The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="5e724-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="5e724-109">Prerequisites</span></span>

<span data-ttu-id="5e724-110">Para concluir este passo a passo usando o ambiente de desenvolvimento do Visual Studio 2012, será necessário:</span><span class="sxs-lookup"><span data-stu-id="5e724-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="5e724-111">Microsoft InfoPath com Visual Studio 2012 instalado.</span><span class="sxs-lookup"><span data-stu-id="5e724-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="5e724-112">Hello World no Visual Studio Tools for Applications</span><span class="sxs-lookup"><span data-stu-id="5e724-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="5e724-113">No passo a passo a seguir, você aprenderá a escrever código no ambiente de desenvolvimento do Visual Studio 2012 para exibir uma caixa de diálogo de alerta simples escrevendo um manipulador de eventos para o evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) da classe [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) , associado ao controle **Botão**.</span><span class="sxs-lookup"><span data-stu-id="5e724-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="5e724-114">Criar um novo projeto e especificar a linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="5e724-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="5e724-115">Inicie o designer do InfoPath e então clique duas vezes no modelo de formulário **Em Branco (Editor do InfoPath)**.</span><span class="sxs-lookup"><span data-stu-id="5e724-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="5e724-116">Para especificar qual linguagem de programação será usada, clique no **Botão do Office**, clique em **Opções de Formulário**, clique em **Programação** na lista **Categoria** e então selecione **Visual Basic** ou **C#** na lista suspensa **Linguagem do código do modelo de formulário**.</span><span class="sxs-lookup"><span data-stu-id="5e724-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="5e724-p103">As outras opções de linguagem de programação da lista **Linguagem do código do modelo de formulário** oferecem compatibilidade com versões anteriores do InfoPath. As opções **C# (Compatível com o InfoPath 2007)** e **Visual Basic (Compatível com o InfoPath 2007)** funcionarão com os procedimentos deste tópico. No entanto, para usar as opções **C# (Compatível com o InfoPath 2003)** e **Visual Basic (Compatível com o InfoPath 2003)**, consulte [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-p103">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath. The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic. However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="5e724-120">Agora você está pronto para adicionar um controle **Botão** e criar seu manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5e724-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="5e724-121">Adicionar um controle Botão e um manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="5e724-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="5e724-122">No grupo **Controles**, clique no controle **Botão** para adicioná-lo ao formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="5e724-p104">Clique duas vezes no controle **Botão**, digite Hello para a propriedade **Rótulo** na guia **Propriedades** da faixa de opções e então clique em **Código Personalizado**. Quando solicitado, salve o formulário e nomeie-o como HelloWorld.</span><span class="sxs-lookup"><span data-stu-id="5e724-p104">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**. When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="5e724-125">Isso abrirá o ambiente **Visual Studio Tools for Applications** com o cursor no manipulador de eventos para o evento [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) do controle **Botão**.</span><span class="sxs-lookup"><span data-stu-id="5e724-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="5e724-126">Agora você está pronto para adicionar código de formulário ao manipulador de eventos para o botão.</span><span class="sxs-lookup"><span data-stu-id="5e724-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="5e724-127">Adicione código do "Hello World" ao manipulador de eventos e visualize o formulário</span><span class="sxs-lookup"><span data-stu-id="5e724-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="5e724-128">No esqueleto do manipulador de eventos, digite:</span><span class="sxs-lookup"><span data-stu-id="5e724-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="5e724-129">O código do seu modelo de formulário deve ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e724-129">The code for your form template should look similar to the following:</span></span>
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. <span data-ttu-id="5e724-130">Alterne para a janela do designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5e724-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="5e724-131">Clique no botão **Visualizar** na guia **Página Inicial**.</span><span class="sxs-lookup"><span data-stu-id="5e724-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="5e724-132">Clique no botão Hello no formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="5e724-133">Será exibida uma caixa de mensagem com o texto "Hello World!"</span><span class="sxs-lookup"><span data-stu-id="5e724-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="5e724-134">O procedimento a seguir mostra como adicionar pontos de interrupção de depuração ao seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="5e724-135">Depurar código de formulário</span><span class="sxs-lookup"><span data-stu-id="5e724-135">Debug form code</span></span>

1. <span data-ttu-id="5e724-136">Alterne novamente para a janela do Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="5e724-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="5e724-137">Clique na barra cinza à esquerda da linha:</span><span class="sxs-lookup"><span data-stu-id="5e724-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="5e724-138">Um círculo vermelho é exibido e a linha de código é realçada para indicar que o tempo de execução será pausado nesse ponto de interrupção no seu código de formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="5e724-139">No menu **Depurar**, clique em **Iniciar Depuração** (ou pressione F5).</span><span class="sxs-lookup"><span data-stu-id="5e724-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="5e724-140">Na janela **Visualizar** do InfoPath, clique no botão Hello do formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="5e724-141">O editor de códigos do Visual Studio 2012 receberá o foco e a linha do ponto de interrupção será realçada.</span><span class="sxs-lookup"><span data-stu-id="5e724-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="5e724-142">No menu **Depurar**, clique em **Ultrapassar** (ou pressione Shift+F8) para continuar a repassar o código.</span><span class="sxs-lookup"><span data-stu-id="5e724-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="5e724-p105">O código do manipulador de eventos é executado e a mensagem "Hello World!" é exibida.</span><span class="sxs-lookup"><span data-stu-id="5e724-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="5e724-145">Clique em **OK** para retornar ao editor de código do Visual Studio 2012 e clique em **Interromper a Depuração** no menu **Depurar** (ou pressione Ctrl+Alt+Break).</span><span class="sxs-lookup"><span data-stu-id="5e724-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="5e724-146">Obtendo o nome do usuário atual</span><span class="sxs-lookup"><span data-stu-id="5e724-146">Getting the Current User's Name</span></span>

<span data-ttu-id="5e724-147">No exemplo a seguir, você aprenderá a usar a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para recuperar o nome do usuário atual e preencher o valor de um controle **Caixa de Texto** usando um manipulador de eventos para o evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e724-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="5e724-148">O preenchimento do controle **Caixa de Texto** é realizado com uma instância da classe [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) para gravar o nome do usuário atual no nó XML ao qual o controle está associado.</span><span class="sxs-lookup"><span data-stu-id="5e724-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="5e724-p106">Primeiro, a propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é chamada para recuperar uma instância da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa o documento XML subjacente do formulário. O objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) então chama o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) que cria o objeto **XPathNavigator** e o posiciona no nó raiz da fonte de dados principal do formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-p106">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form. The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="5e724-p107">O método [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) da classe **XPathNavigator** é chamado para selecionar o campo funcionário na fonte de dados do formulário. Por fim, o método [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) é chamado para definir o valor do campo com a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e724-p107">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source. Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="5e724-153">Confira mais informações sobre o trabalho com **System.Xml** em modelos de formulário de código gerenciado em [Trabalhar com as classes XPathNavigator e XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-153">For more information on working with **System.Xml** in managed code form templates, see [How to: Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="5e724-154">Adicionar um manipulador de eventos de Carregamento</span><span class="sxs-lookup"><span data-stu-id="5e724-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="5e724-155">Abra o modelo de formulário HelloWorld criado no passo a passo anterior no designer do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="5e724-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="5e724-156">Na guia **Exibir**, selecione **Mostrar Campos**.</span><span class="sxs-lookup"><span data-stu-id="5e724-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="5e724-157">Clique com o botão direito do mouse na pasta **myFields** e então clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="5e724-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="5e724-158">Em **Nome**, digite funcionário e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e724-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="5e724-159">Arraste o campo funcionário para a exibição.</span><span class="sxs-lookup"><span data-stu-id="5e724-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="5e724-160">Na guia **Desenvolvedor**, clique em **Evento Loading**.</span><span class="sxs-lookup"><span data-stu-id="5e724-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="5e724-161">Isso criará um manipulador de eventos para o evento [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) e moverá o foco para esse manipulador de eventos no editor de códigos.</span><span class="sxs-lookup"><span data-stu-id="5e724-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="5e724-162">No editor de códigos, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5e724-162">In the code editor, type the following:</span></span>
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. <span data-ttu-id="5e724-163">Alterne para a janela de design de formulários do InfoPath e então clique no botão **Visualizar** na guia **Página Inicial** para visualizar o formulário.</span><span class="sxs-lookup"><span data-stu-id="5e724-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="5e724-164">O campo funcionário deverá ser automaticamente preenchido com o seu nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="5e724-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="5e724-165">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="5e724-165">Next steps</span></span>

- <span data-ttu-id="5e724-166">Confira mais informações sobre como trabalhar com manipuladores de eventos para outros controles e eventos em [Adicionar um Manipulador de Eventos](how-to-add-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-166">For information about working with event handlers for other controls and events, see [How to: Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="5e724-167">Confira mais informações sobre como visualizar e depurar códigos em modelos de formulário em [Visualizar e depurar modelos de formulário do InfoPath com código](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-167">For more information about previewing and debugging code in form templates, see [How to: Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="5e724-168">Confira mais informações sobre como implantar um modelo de formulário de código gerenciado em [Implantar os modelos de formulário do InfoPath com código](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-168">For information about how to deploy a managed-code form template, see [How to: Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="5e724-169">Para saber mais sobre o modelo de objeto e as tarefas comuns de programação do InfoPath em modelos de formulário de código gerenciado, consulte [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="5e724-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e724-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e724-170">See also</span></span>

- [<span data-ttu-id="5e724-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="5e724-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)


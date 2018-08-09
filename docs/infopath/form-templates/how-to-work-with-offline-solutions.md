---
title: Trabalhar com soluções offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- soluções offline [infopath 2007], soluções [InfoPath 2007], offline, InfoPath 2007, offline soluções
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: O modelo de objeto do InfoPath fornece a propriedade MachineOnlineState da classe Application que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede. Verificando o valor da propriedade MachineOnlineState, seu código de formulário pode executar ações diferentes dependendo do estado da conexão.
ms.openlocfilehash: fcdaae31dd6a0c76cf1c453f267be430a2b34bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765616"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="e352c-105">Trabalhar com soluções offline</span><span class="sxs-lookup"><span data-stu-id="e352c-105">Work with offline solutions</span></span>

<span data-ttu-id="e352c-106">O modelo de objeto do InfoPath fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e352c-106">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="e352c-107">Verificando o valor da propriedade **MachineOnlineState** , seu código de formulário pode executar ações diferentes dependendo do estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="e352c-107">By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="e352c-108">Use a propriedade MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="e352c-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="e352c-109">O exemplo a seguir mostra como você pode adicionar lógica para seu código de formulário que determina como enviar um formulário baseado em se o computador do usuário está online ou offline.</span><span class="sxs-lookup"><span data-stu-id="e352c-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="e352c-110">Este exemplo pressupõe que você tenha criado um formulário para enviar um relatório de vendas que contém um campo denominado período que especifica o mês e ano abordados no relatório.</span><span class="sxs-lookup"><span data-stu-id="e352c-110">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report.</span></span> <span data-ttu-id="e352c-111">Ele também pressupõe que você já tenha definido uma conexão de dados e a lógica para o envio do relatório quando o usuário está online.</span><span class="sxs-lookup"><span data-stu-id="e352c-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="e352c-112">Adicionar uma conexão de dados que envia o formulário como um anexo em uma mensagem de email</span><span class="sxs-lookup"><span data-stu-id="e352c-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="e352c-113">Crie um modelo de formulário do InfoPath usando o modelo **em branco (InfoPath Editor)** .</span><span class="sxs-lookup"><span data-stu-id="e352c-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="e352c-114">No modo de design do InfoPath, clique em **Conexões de dados** , na guia **dados** .</span><span class="sxs-lookup"><span data-stu-id="e352c-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="e352c-115">Na caixa de diálogo **Conexões de dados** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="e352c-116">No **Assistente de Conexão de dados**, clique em **Enviar dados**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="e352c-117">Na próxima página do assistente, clique em **como uma mensagem de email**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="e352c-118">Na próxima página do assistente, digite seu endereço de email na caixa **para** .</span><span class="sxs-lookup"><span data-stu-id="e352c-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="e352c-119">Na caixa **assunto** , faça o seguinte para o ponto de venda combinado com o relatório de vendas de texto:</span><span class="sxs-lookup"><span data-stu-id="e352c-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="e352c-120">Clique no botão de **fórmula** ao lado da caixa **assunto** .</span><span class="sxs-lookup"><span data-stu-id="e352c-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="e352c-121">Na caixa de diálogo **Inserir Fórmula** , clique em **Inserir função**.</span><span class="sxs-lookup"><span data-stu-id="e352c-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="e352c-122">Na caixa de diálogo **Inserir função** , clique em **texto** na lista **categorias** e, em seguida, clique duas vezes em **concat** na lista de **funções** .</span><span class="sxs-lookup"><span data-stu-id="e352c-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="e352c-123">Substitua a primeira instância do **clique duas vezes para inserir campo** o seguinte (inclua as aspas): ' relatório Vendas: '</span><span class="sxs-lookup"><span data-stu-id="e352c-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="e352c-124">Clique duas vezes a segunda instância do **clique duas vezes para inserir campo**.</span><span class="sxs-lookup"><span data-stu-id="e352c-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="e352c-125">Na caixa de diálogo **Selecionar campo ou grupo** , selecione o campo período.</span><span class="sxs-lookup"><span data-stu-id="e352c-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="e352c-126">Exclua a instância final do **clique duas vezes para inserir campo**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="e352c-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="e352c-127">No assistente, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="e352c-128">Na próxima página do assistente, clique no botão de **fórmula** ao lado da caixa **Nome do anexo** e, em seguida, repita as etapas acima para criar a fórmula concat ("Relatório de vendas" -, período) e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="e352c-129">Na última página do assistente, digite o envio de Email na caixa **Digite um nome para essa conexão de dados** e clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="e352c-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="e352c-130">Adicionar lógica para enviar o formulário, dependendo do estado conectado de um computador do usuário</span><span class="sxs-lookup"><span data-stu-id="e352c-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="e352c-131">No modo de design do InfoPath, clique em **Opções de envio** , na guia **dados** .</span><span class="sxs-lookup"><span data-stu-id="e352c-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="e352c-132">Na caixa de diálogo **Opções de envio** , clique em **Permitir que os usuários enviem este formulário**, selecione **Executar ação personalizada usando o código**, clique em **Editar código**.</span><span class="sxs-lookup"><span data-stu-id="e352c-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="e352c-133">Adicione as seguintes duas funções abaixo o manipulador de eventos de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) :</span><span class="sxs-lookup"><span data-stu-id="e352c-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. <span data-ttu-id="e352c-134">Adicione a seguinte instrução **se** para a função de manipulador de eventos de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e352c-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a><span data-ttu-id="e352c-135">Testar o código</span><span class="sxs-lookup"><span data-stu-id="e352c-135">Test the code</span></span>

1. <span data-ttu-id="e352c-136">No menu **Depurar** , clique em **Iniciar depuração**.</span><span class="sxs-lookup"><span data-stu-id="e352c-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="e352c-137">Preencha o formulário.</span><span class="sxs-lookup"><span data-stu-id="e352c-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="e352c-138">Inicie o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e352c-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="e352c-139">No Internet Explorer, clique em **trabalhar offline** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="e352c-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="e352c-140">No InfoPath, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="e352c-141">Você deverá ver uma mensagem que o formulário será enviado como uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="e352c-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="e352c-142">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e352c-142">Click **Send**.</span></span> <span data-ttu-id="e352c-143">Você verá uma mensagem informando que o formulário tiver sido enviado offline e será enviado ao se conectar à rede.</span><span class="sxs-lookup"><span data-stu-id="e352c-143">You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e352c-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e352c-144">See also</span></span>

- [<span data-ttu-id="e352c-145">Criar um modelo de formulário para uso offline</span><span class="sxs-lookup"><span data-stu-id="e352c-145">Design a form template for offline use</span></span>](http://office.microsoft.com/en-us/infopath/HA102117391033.aspx?pid=CH100341121033)


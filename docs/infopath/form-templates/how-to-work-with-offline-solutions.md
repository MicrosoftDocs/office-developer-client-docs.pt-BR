---
title: Trabalhar com soluções offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- soluções offline [infopath 2007], soluções [InfoPath 2007], offline,InfoPath 2007, soluções offline
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: O modelo de objeto do InfoPath fornece a propriedade MachineOnlineState da classe Application que permite que seu código de formulário verifique se o computador do usuário está conectado à rede. Verificando o valor da propriedade MachineOnlineState, seu código de formulário pode executar ações diferentes dependendo do estado da conexão.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436136"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="14146-105">Trabalhar com soluções offline</span><span class="sxs-lookup"><span data-stu-id="14146-105">Work with offline solutions</span></span>

<span data-ttu-id="14146-106">O modelo de objeto do InfoPath fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que permite que seu código de formulário verifique se o computador do usuário está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="14146-106">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="14146-107">Verificando o valor da **propriedade MachineOnlineState,** seu código de formulário pode executar ações diferentes dependendo do estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="14146-107">By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="14146-108">Usando a propriedade MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="14146-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="14146-109">O exemplo a seguir mostra como você pode adicionar lógica ao código do formulário que determina como enviar um formulário com base em se o computador do usuário está online ou offline.</span><span class="sxs-lookup"><span data-stu-id="14146-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="14146-110">Este exemplo assume que você criou um formulário para enviar um relatório de vendas que contém um campo denominado período que especifica o mês e o ano cobertos no relatório.</span><span class="sxs-lookup"><span data-stu-id="14146-110">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report.</span></span> <span data-ttu-id="14146-111">Ele também presume que você já tenha definido uma conexão de dados e a lógica para enviar o relatório quando o usuário estiver online.</span><span class="sxs-lookup"><span data-stu-id="14146-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="14146-112">Adicionar uma conexão de dados que envia o formulário como um anexo a uma mensagem de email</span><span class="sxs-lookup"><span data-stu-id="14146-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="14146-113">Crie um modelo de formulário do InfoPath usando o **modelo em Branco (Editor do InfoPath).**</span><span class="sxs-lookup"><span data-stu-id="14146-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="14146-114">No modo de design do InfoPath, clique em **Conexões de** Dados na **guia** Dados.</span><span class="sxs-lookup"><span data-stu-id="14146-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="14146-115">Na caixa **de diálogo Conexões** de Dados, clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="14146-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="14146-116">No Assistente **para Conexão de Dados,** clique **em Enviar dados** e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="14146-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="14146-117">Na próxima página do assistente, clique **em Como uma mensagem de email** e clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="14146-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="14146-118">Na próxima página do assistente, digite seu endereço de email na **caixa** Para.</span><span class="sxs-lookup"><span data-stu-id="14146-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="14146-119">Na caixa **Assunto,** faça o seguinte para combinar o período de vendas com o texto Relatório de Vendas:</span><span class="sxs-lookup"><span data-stu-id="14146-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="14146-120">Clique no **botão** Fórmula ao lado da **caixa** Assunto.</span><span class="sxs-lookup"><span data-stu-id="14146-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="14146-121">Na caixa de diálogo Inserir **Fórmula,** clique em **Inserir Função.**</span><span class="sxs-lookup"><span data-stu-id="14146-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="14146-122">Na caixa **de diálogo Inserir Função,** clique em **Texto**  na lista **Categorias** e clique duas vezes na lista Funções. </span><span class="sxs-lookup"><span data-stu-id="14146-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="14146-123">Substitua a primeira instância do **clique duplo para inserir** o campo pelo seguinte (inclua as aspas simples): 'Sales Report: '</span><span class="sxs-lookup"><span data-stu-id="14146-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="14146-124">Clique duas vezes na segunda instância do **clique duplo para inserir o campo.**</span><span class="sxs-lookup"><span data-stu-id="14146-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="14146-125">Na caixa **de diálogo Selecionar um Campo ou Grupo,** selecione o campo ponto final.</span><span class="sxs-lookup"><span data-stu-id="14146-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="14146-126">Exclua a instância final **do clique duplo para inserir o campo** e clique em **OK.**</span><span class="sxs-lookup"><span data-stu-id="14146-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="14146-127">No assistente, clique em **Próximo.**</span><span class="sxs-lookup"><span data-stu-id="14146-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="14146-128">Na próxima página do assistente,  clique no  botão Fórmula ao lado da caixa Nome do Anexo e repita as etapas acima para criar a fórmula concat("Sales Report - ", period) e clique em **Next**.</span><span class="sxs-lookup"><span data-stu-id="14146-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="14146-129">Na última página do assistente, digite Enviar Email na caixa Inserir um nome para **essa** conexão de dados e clique em **Concluir.**</span><span class="sxs-lookup"><span data-stu-id="14146-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="14146-130">Adicionar lógica para enviar o formulário dependendo do estado conectado do computador de um usuário</span><span class="sxs-lookup"><span data-stu-id="14146-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="14146-131">No modo de design do InfoPath, clique **em Opções de** Envio na **guia** Dados.</span><span class="sxs-lookup"><span data-stu-id="14146-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="14146-132">Na caixa **de diálogo Opções de** Envio, clique em Permitir que os usuários enviem este **formulário,** selecione Executar ação personalizada usando **Código,** clique em **Editar Código.**</span><span class="sxs-lookup"><span data-stu-id="14146-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="14146-133">Adicione as duas funções a seguir abaixo do manipulador [de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) eventos Enviar:</span><span class="sxs-lookup"><span data-stu-id="14146-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
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

4. <span data-ttu-id="14146-134">Adicione a **instrução if** a seguir à [função de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) manipulador de eventos Enviar.</span><span class="sxs-lookup"><span data-stu-id="14146-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="14146-135">Testar o código</span><span class="sxs-lookup"><span data-stu-id="14146-135">Test the code</span></span>

1. <span data-ttu-id="14146-136">No menu **Depurar,** clique **em Iniciar Depuração.**</span><span class="sxs-lookup"><span data-stu-id="14146-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="14146-137">Preencha o formulário.</span><span class="sxs-lookup"><span data-stu-id="14146-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="14146-138">Inicie o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="14146-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="14146-139">No Internet Explorer, clique **em Trabalhar offline** no menu Arquivo. </span><span class="sxs-lookup"><span data-stu-id="14146-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="14146-140">No InfoPath, clique em **Enviar.**</span><span class="sxs-lookup"><span data-stu-id="14146-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="14146-141">Você verá uma mensagem de que o formulário será enviado como uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="14146-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="14146-142">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="14146-142">Click **Send**.</span></span> <span data-ttu-id="14146-143">Você verá uma mensagem informando que o formulário foi enviado offline e será enviado quando você se conectar à rede.</span><span class="sxs-lookup"><span data-stu-id="14146-143">You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14146-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="14146-144">See also</span></span>

- [<span data-ttu-id="14146-145">Criar um modelo de formulário para uso offline</span><span class="sxs-lookup"><span data-stu-id="14146-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)


---
title: Trabalhar com as soluções offline usando o modelo de objeto do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- soluções [infopath 2007], offline, offline soluções [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, soluções offline
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: O modelo de objeto compatível com o InfoPath 2003 fornece a propriedade MachineOnlineState do objeto Application que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede. Seu código de formulário pode realizar ações diferentes dependendo do estado da conexão.
ms.openlocfilehash: 858b5d317cf5245dbfb447fa9e118a11ecbe7eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765612"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="3b28b-105">Trabalhar com as soluções offline usando o modelo de objeto do InfoPath</span><span class="sxs-lookup"><span data-stu-id="3b28b-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="3b28b-106">O modelo de objeto compatível com o InfoPath 2003 fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) do objeto [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="3b28b-106">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network.</span></span> <span data-ttu-id="3b28b-107">Seu código de formulário pode realizar ações diferentes dependendo do estado da conexão.</span><span class="sxs-lookup"><span data-stu-id="3b28b-107">Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="3b28b-108">Use a propriedade MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="3b28b-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="3b28b-109">O exemplo a seguir mostra como você pode adicionar lógica para seu código de formulário que determina como enviar um formulário baseado em se o computador do usuário está online ou offline.</span><span class="sxs-lookup"><span data-stu-id="3b28b-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="3b28b-110">Este exemplo pressupõe que você tenha criado um formulário para enviar um relatório de vendas que contém um campo chamado "período" que especifica o mês e ano abordados no relatório.</span><span class="sxs-lookup"><span data-stu-id="3b28b-110">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report.</span></span> <span data-ttu-id="3b28b-111">Ele também pressupõe que você já tenha definido uma conexão de dados e a lógica para o envio do relatório quando o usuário está online.</span><span class="sxs-lookup"><span data-stu-id="3b28b-111">It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="3b28b-112">Adicionar uma conexão de dados que envia o formulário como um anexo em uma mensagem de email</span><span class="sxs-lookup"><span data-stu-id="3b28b-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="3b28b-113">Criar ou abrir um modelo de formulário de código gerenciado do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="3b28b-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="3b28b-114">No modo de design do InfoPath, na guia **dados** , clique em **Conexões de dados**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="3b28b-115">Na caixa de diálogo **Conexões de dados** , clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="3b28b-116">No **Assistente de Conexão de dados**, clique em **Enviar dados**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="3b28b-117">Na próxima página do assistente, clique em **como uma mensagem de email**e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="3b28b-118">Na próxima página do assistente, digite seu endereço de email na caixa **para** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="3b28b-119">Na caixa **assunto** , faça o seguinte para o ponto de venda combinado com o relatório de vendas de texto:</span><span class="sxs-lookup"><span data-stu-id="3b28b-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="3b28b-120">Clique no botão de **fórmula** ao lado da caixa **assunto** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="3b28b-121">Na caixa de diálogo **Inserir Fórmula** , clique em **Inserir função**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="3b28b-122">Na caixa de diálogo **Inserir função** , clique em **texto** na lista **categorias** e, em seguida, clique duas vezes em **concat** na lista de **funções** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="3b28b-123">Substitua a primeira instância do **clique duas vezes para inserir campo** o seguinte (inclua as aspas): ' relatório Vendas: '</span><span class="sxs-lookup"><span data-stu-id="3b28b-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="3b28b-124">Clique duas vezes a segunda instância do **clique duas vezes para inserir campo**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="3b28b-125">Na caixa de diálogo **Selecionar campo ou grupo** , selecione o campo período.</span><span class="sxs-lookup"><span data-stu-id="3b28b-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="3b28b-126">Exclua a instância final do **clique duas vezes para inserir campo**e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="3b28b-127">No assistente, clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="3b28b-128">Na próxima página do assistente, digite 'Enviar Email' na caixa **Digite um nome para essa conexão de dados** e clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="3b28b-129">Adicionar lógica para enviar o formulário, dependendo do estado conectado de um computador do usuário</span><span class="sxs-lookup"><span data-stu-id="3b28b-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="3b28b-130">No modo de design do InfoPath, na guia **dados** , clique em **Opções de envio**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="3b28b-131">Na caixa de diálogo **Opções de envio** , clique em **Permitir que os usuários enviem este formulário**e, em seguida, selecione **Executar ação personalizada usando o código**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="3b28b-132">Clique no botão **Editar código** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="3b28b-133">Adicione as seguintes duas funções abaixo o manipulador de eventos [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) :</span><span class="sxs-lookup"><span data-stu-id="3b28b-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. <span data-ttu-id="3b28b-134">Adicione a seguinte instrução **se** para a função do manipulador de eventos **OnSubmitRequest** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a><span data-ttu-id="3b28b-135">Testar o código</span><span class="sxs-lookup"><span data-stu-id="3b28b-135">Test the code</span></span>

1. <span data-ttu-id="3b28b-136">No designer do InfoPath, clique em **Visualizar** na guia **página inicial** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="3b28b-137">Preencha o formulário.</span><span class="sxs-lookup"><span data-stu-id="3b28b-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="3b28b-138">Inicie o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b28b-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="3b28b-139">No Internet Explorer, clique em **trabalhar offline** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="3b28b-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="3b28b-140">No InfoPath, clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="3b28b-141">Você deverá ver uma mensagem que o formulário será enviado como uma mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="3b28b-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="3b28b-142">Clique em **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="3b28b-142">Click **Send**.</span></span> <span data-ttu-id="3b28b-143">Você verá uma mensagem informando que o formulário foi enviado offline.</span><span class="sxs-lookup"><span data-stu-id="3b28b-143">You should see a message stating that the form has been submitted offline.</span></span>
    


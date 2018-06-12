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
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Trabalhar com as soluções offline usando o modelo de objeto do InfoPath

O modelo de objeto compatível com o InfoPath 2003 fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) do objeto [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede. Seu código de formulário pode realizar ações diferentes dependendo do estado da conexão. 
  
## <a name="using-the-machineonlinestate-property"></a>Use a propriedade MachineOnlineState

O exemplo a seguir mostra como você pode adicionar lógica para seu código de formulário que determina como enviar um formulário baseado em se o computador do usuário está online ou offline.
  
Este exemplo pressupõe que você tenha criado um formulário para enviar um relatório de vendas que contém um campo chamado "período" que especifica o mês e ano abordados no relatório. Ele também pressupõe que você já tenha definido uma conexão de dados e a lógica para o envio do relatório quando o usuário está online.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adicionar uma conexão de dados que envia o formulário como um anexo em uma mensagem de email

1. Criar ou abrir um modelo de formulário de código gerenciado do InfoPath.
    
2. No modo de design do InfoPath, na guia **dados** , clique em **Conexões de dados**.
    
3. Na caixa de diálogo **Conexões de dados** , clique em **Adicionar**.
    
4. No **Assistente de Conexão de dados**, clique em **Enviar dados**e clique em **Avançar**.
    
5. Na próxima página do assistente, clique em **como uma mensagem de email**e clique em **Avançar**.
    
6. Na próxima página do assistente, digite seu endereço de email na caixa **para** . 
    
7. Na caixa **assunto** , faça o seguinte para o ponto de venda combinado com o relatório de vendas de texto: 
    
   1. Clique no botão de **fórmula** ao lado da caixa **assunto** . 
      
   2. Na caixa de diálogo **Inserir Fórmula** , clique em **Inserir função**.
      
   3. Na caixa de diálogo **Inserir função** , clique em **texto** na lista **categorias** e, em seguida, clique duas vezes em **concat** na lista de **funções** . 
      
   4. Substitua a primeira instância do **clique duas vezes para inserir campo** o seguinte (inclua as aspas): ' relatório Vendas: ' 
      
   5. Clique duas vezes a segunda instância do **clique duas vezes para inserir campo**.
      
   6. Na caixa de diálogo **Selecionar campo ou grupo** , selecione o campo período. 
      
   7. Exclua a instância final do **clique duas vezes para inserir campo**e, em seguida, clique em **Okey**.
    
8. No assistente, clique em **Avançar**.
    
9. Na próxima página do assistente, digite 'Enviar Email' na caixa **Digite um nome para essa conexão de dados** e clique em **Concluir**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Adicionar lógica para enviar o formulário, dependendo do estado conectado de um computador do usuário

1. No modo de design do InfoPath, na guia **dados** , clique em **Opções de envio**.
    
2. Na caixa de diálogo **Opções de envio** , clique em **Permitir que os usuários enviem este formulário**e, em seguida, selecione **Executar ação personalizada usando o código**.
    
3. Clique no botão **Editar código** . 
    
4. Adicione as seguintes duas funções abaixo o manipulador de eventos [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) : 
    
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

5. Adicione a seguinte instrução **se** para a função do manipulador de eventos **OnSubmitRequest** . 
    
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

### <a name="test-the-code"></a>Testar o código

1. No designer do InfoPath, clique em **Visualizar** na guia **página inicial** . 
    
2. Preencha o formulário.
    
3. Inicie o Microsoft Internet Explorer.
    
4. No Internet Explorer, clique em **trabalhar offline** no menu **arquivo** . 
    
5. No InfoPath, clique em **Enviar**. Você deverá ver uma mensagem que o formulário será enviado como uma mensagem de email.
    
6. Clique em **Enviar**. Você verá uma mensagem informando que o formulário foi enviado offline.
    


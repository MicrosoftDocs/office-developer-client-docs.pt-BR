---
title: Trabalhar com soluções offline usando o modelo de objeto do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- soluções [infopath 2007], offline,soluções offline [InfoPath 2007], modelos de formulário compatíveis com InfoPath 2003, modelos de formulário compatíveis com InfoPath 2003, soluções offline
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: O modelo de objeto compatível com InfoPath 2003 fornece a propriedade MachineOnlineState do objeto Application que permite que seu código de formulário verifique se o computador do usuário está conectado à rede. Seu código de formulário pode executar diferentes ações dependendo do estado da conexão.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429240"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Trabalhar com soluções offline usando o modelo de objeto do InfoPath

O modelo de objeto compatível com InfoPath 2003 fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) do objeto [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) que permite que seu código de formulário verifique se o computador do usuário está conectado à rede. Seu código de formulário pode executar ações diferentes dependendo do estado da conexão. 
  
## <a name="using-the-machineonlinestate-property"></a>Usando a propriedade MachineOnlineState

O exemplo a seguir mostra como você pode adicionar lógica ao código do formulário que determina como enviar um formulário com base em se o computador do usuário está online ou offline.
  
Este exemplo assume que você criou um formulário para enviar um relatório de vendas que contém um campo chamado "período" que especifica o mês e o ano cobertos no relatório. Ele também presume que você já tenha definido uma conexão de dados e a lógica para enviar o relatório quando o usuário estiver online.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adicionar uma conexão de dados que envia o formulário como um anexo a uma mensagem de email

1. Criar ou abrir um modelo de formulário de código gerenciado do InfoPath.
    
2. No modo de design do InfoPath, na guia **Dados,** clique em **Conexões de Dados.**
    
3. Na caixa **de diálogo Conexões** de Dados, clique em **Adicionar**.
    
4. No Assistente **para Conexão de Dados,** clique **em Enviar dados** e clique em **Próximo.**
    
5. Na próxima página do assistente, clique **em Como uma mensagem de email** e clique em **Próximo.**
    
6. Na próxima página do assistente, digite seu endereço de email na **caixa** Para. 
    
7. Na caixa **Assunto,** faça o seguinte para combinar o período de vendas com o texto Relatório de Vendas: 
    
   1. Clique no **botão** Fórmula ao lado da **caixa** Assunto. 
      
   2. Na caixa de diálogo Inserir **Fórmula,** clique em **Inserir Função.**
      
   3. Na caixa **de diálogo Inserir Função,** clique em **Texto**  na lista **Categorias** e clique duas vezes na lista Funções.  
      
   4. Substitua a primeira instância do **clique duplo para inserir** o campo pelo seguinte (inclua as aspas simples): 'Sales Report: ' 
      
   5. Clique duas vezes na segunda instância do **clique duplo para inserir o campo.**
      
   6. Na caixa **de diálogo Selecionar um Campo ou Grupo,** selecione o campo ponto final. 
      
   7. Exclua a instância final **do clique duplo para inserir o campo** e clique em **OK.**
    
8. No assistente, clique em **Próximo.**
    
9. Na próxima página do assistente, digite 'Enviar Email' na caixa Inserir um nome para **essa** conexão de dados e clique em **Concluir.**
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Adicionar lógica para enviar o formulário dependendo do estado conectado do computador de um usuário

1. No modo de design do InfoPath, na **guia Dados,** clique em **Opções de Envio.**
    
2. Na caixa **de diálogo Opções de** Envio, clique em Permitir que os usuários **enviem este formulário** e selecione Executar ação personalizada usando **Código.**
    
3. Clique no **botão Editar** Código. 
    
4. Adicione as duas funções a seguir abaixo do manipulador de eventos [OnSubmitRequest:](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) 
    
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

5. Adicione a **instrução if** a seguir à função de manipulador de eventos **OnSubmitRequest.** 
    
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

1. No designer do InfoPath, clique **em Visualizar** na **guia** Página Home. 
    
2. Preencha o formulário.
    
3. Inicie o Microsoft Internet Explorer.
    
4. No Internet Explorer, clique **em Trabalhar offline** no menu Arquivo.  
    
5. No InfoPath, clique em **Enviar.** Você verá uma mensagem de que o formulário será enviado como uma mensagem de email.
    
6. Clique em **Enviar**. Você verá uma mensagem informando que o formulário foi enviado offline.
    


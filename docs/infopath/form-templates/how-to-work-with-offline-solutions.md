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
# <a name="work-with-offline-solutions"></a>Trabalhar com soluções offline

O modelo de objeto do InfoPath fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que permite que seu código de formulário verifique se o computador do usuário está conectado à rede. Verificando o valor da **propriedade MachineOnlineState,** seu código de formulário pode executar ações diferentes dependendo do estado da conexão. 
  
## <a name="using-the-machineonlinestate-property"></a>Usando a propriedade MachineOnlineState

O exemplo a seguir mostra como você pode adicionar lógica ao código do formulário que determina como enviar um formulário com base em se o computador do usuário está online ou offline.
  
Este exemplo assume que você criou um formulário para enviar um relatório de vendas que contém um campo denominado período que especifica o mês e o ano cobertos no relatório. Ele também presume que você já tenha definido uma conexão de dados e a lógica para enviar o relatório quando o usuário estiver online. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adicionar uma conexão de dados que envia o formulário como um anexo a uma mensagem de email

1. Crie um modelo de formulário do InfoPath usando o **modelo em Branco (Editor do InfoPath).** 
    
2. No modo de design do InfoPath, clique em **Conexões de** Dados na **guia** Dados. 
    
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
    
9. Na próxima página do assistente,  clique no  botão Fórmula ao lado da caixa Nome do Anexo e repita as etapas acima para criar a fórmula concat("Sales Report - ", period) e clique em **Next**.
    
10. Na última página do assistente, digite Enviar Email na caixa Inserir um nome para **essa** conexão de dados e clique em **Concluir.**
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Adicionar lógica para enviar o formulário dependendo do estado conectado do computador de um usuário

1. No modo de design do InfoPath, clique **em Opções de** Envio na **guia** Dados. 
    
2. Na caixa **de diálogo Opções de** Envio, clique em Permitir que os usuários enviem este **formulário,** selecione Executar ação personalizada usando **Código,** clique em **Editar Código.**
    
3. Adicione as duas funções a seguir abaixo do manipulador [de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) eventos Enviar: 
    
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

4. Adicione a **instrução if** a seguir à [função de](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) manipulador de eventos Enviar. 
    
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

### <a name="test-the-code"></a>Testar o código

1. No menu **Depurar,** clique **em Iniciar Depuração.**
    
2. Preencha o formulário.
    
3. Inicie o Microsoft Internet Explorer.
    
4. No Internet Explorer, clique **em Trabalhar offline** no menu Arquivo.  
    
5. No InfoPath, clique em **Enviar.** Você verá uma mensagem de que o formulário será enviado como uma mensagem de email.
    
6. Clique em **Enviar**. Você verá uma mensagem informando que o formulário foi enviado offline e será enviado quando você se conectar à rede.
    
## <a name="see-also"></a>Confira também

- [Criar um modelo de formulário para uso offline](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)


---
title: Trabalhar com soluções offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- soluções offline [InfoPath 2007], soluções [InfoPath 2007], offline, InfoPath 2007, soluções offline
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: O modelo de objeto do InfoPath fornece a propriedade MachineOnlineState da classe Application que permite que o código do formulário Verifique se o computador do usuário está conectado à rede. Verificando o valor da propriedade MachineOnlineState, seu código de formulário pode executar ações diferentes dependendo do estado da conexão.
ms.openlocfilehash: eb2903c2445a61be803c0d7a2f5ddd7ac7a912ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299812"
---
# <a name="work-with-offline-solutions"></a>Trabalhar com soluções offline

O modelo de objeto do InfoPath fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que permite que o código do formulário Verifique se o computador do usuário está conectado à rede. Verificando o valor da propriedade **MachineOnlineState** , seu código de formulário pode executar ações diferentes dependendo do estado da conexão. 
  
## <a name="using-the-machineonlinestate-property"></a>Usando a propriedade MachineOnlineState

O exemplo a seguir mostra como você pode adicionar lógica ao seu código de formulário que determina como enviar um formulário com base em se o computador do usuário está online ou offline.
  
Este exemplo pressupõe que você tenha criado um formulário para enviar um relatório de vendas que contém um campo chamado period que especifica o mês e o ano cobertos no relatório. Também presume que você já tenha definido uma conexão de dados e a lógica para o envio do relatório quando o usuário estiver online. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adicionar uma conexão de dados que envia o formulário como um anexo a uma mensagem de email

1. Criar um modelo de formulário do InfoPath usando o modelo **em branco (editor do InfoPath)** . 
    
2. No modo de design do InfoPath, clique em **conexões de dados** na guia **dados** . 
    
3. Na caixa de diálogo **conexões de dados** , clique em **Adicionar**.
    
4. No **Assistente para conexão de dados**, clique em **enviar dados**e, em seguida, clique em **Avançar**.
    
5. Na próxima página do assistente, clique em **como uma mensagem de email**e clique em **Avançar**.
    
6. Na próxima página do assistente, digite seu endereço de email na caixa **para** . 
    
7. Na caixa **assunto** , faça o seguinte para combinar o período de vendas com o relatório de vendas de texto: 
    
   1. Clique no botão de **fórmula** ao lado da caixa **assunto** . 
      
   2. Na caixa de diálogo **Inserir fórmula** , clique em **Inserir função**.
      
   3. Na caixa de diálogo **Inserir função** , clique em **texto** na lista **categorias** e, em seguida, clique duas vezes em **concat** na lista **funções** . 
      
   4. Substitua a primeira instância do **clique duplo para inserir o campo** com o seguinte (inclua as aspas simples): ' relatório de vendas: ' 
      
   5. Clique duas vezes na segunda instância de **clique duplo para inserir o campo**.
      
   6. Na caixa de diálogo **selecionar um campo ou grupo** , selecione o campo período. 
      
   7. Exclua a instância final do **clique duplo para inserir campo**e, em seguida, clique em **OK**.
    
8. No assistente, clique em **Avançar**.
    
9. Na próxima página do assistente, clique no botão de **fórmula** ao lado da caixa **nome do anexo** e, em seguida, repita as etapas acima para criar a fórmula Concat ("relatório de vendas-", ponto) e clique em **Avançar**.
    
10. Na última página do assistente, digite envio de email na caixa **digite um nome para esta conexão de dados** e clique em **concluir**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Adicionar lógica para enviar o formulário dependendo do estado conectado do computador de um usuário

1. No modo de design do InfoPath, clique em **Opções de envio** na guia **dados** . 
    
2. Na caixa de diálogo **Opções de envio** , clique em **permitir que os usuários enviem este formulário**, selecione **executar ação personalizada usando código**, clique em **Editar código**.
    
3. Adicione as duas seguintes funções abaixo do manipulador de eventos [Enviar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) : 
    
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

4. Adicione a instrução **If** a seguir à função de manipulador de eventos [Enviar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) . 
    
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

1. No menu **depurar** , clique em **Iniciar Depuração**.
    
2. Preencha o formulário.
    
3. Inicie o Microsoft Internet Explorer.
    
4. No Internet Explorer, clique em **trabalhar offline** no menu **arquivo** . 
    
5. No InfoPath, clique em **Enviar**. Você verá uma mensagem de que o formulário será enviado como uma mensagem de email.
    
6. Clique em **Enviar**. Você verá uma mensagem informando que o formulário foi enviado offline e será enviado quando você se conectar à rede.
    
## <a name="see-also"></a>Confira também

- [Criar um modelo de formulário para uso offline](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)


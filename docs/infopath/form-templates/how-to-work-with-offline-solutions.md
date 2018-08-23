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
ms.openlocfilehash: ab149b488d2b2df1e91ba2cb435960c6749ecefb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574556"
---
# <a name="work-with-offline-solutions"></a>Trabalhar com soluções offline

O modelo de objeto do InfoPath fornece a propriedade [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) que permite que o seu código de formulário para verificar se o computador do usuário está conectado à rede. Verificando o valor da propriedade **MachineOnlineState** , seu código de formulário pode executar ações diferentes dependendo do estado da conexão. 
  
## <a name="using-the-machineonlinestate-property"></a>Use a propriedade MachineOnlineState

O exemplo a seguir mostra como você pode adicionar lógica para seu código de formulário que determina como enviar um formulário baseado em se o computador do usuário está online ou offline.
  
Este exemplo pressupõe que você tenha criado um formulário para enviar um relatório de vendas que contém um campo denominado período que especifica o mês e ano abordados no relatório. Ele também pressupõe que você já tenha definido uma conexão de dados e a lógica para o envio do relatório quando o usuário está online. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Adicionar uma conexão de dados que envia o formulário como um anexo em uma mensagem de email

1. Crie um modelo de formulário do InfoPath usando o modelo **em branco (InfoPath Editor)** . 
    
2. No modo de design do InfoPath, clique em **Conexões de dados** , na guia **dados** . 
    
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
    
9. Na próxima página do assistente, clique no botão de **fórmula** ao lado da caixa **Nome do anexo** e, em seguida, repita as etapas acima para criar a fórmula concat ("Relatório de vendas" -, período) e clique em **Avançar**.
    
10. Na última página do assistente, digite o envio de Email na caixa **Digite um nome para essa conexão de dados** e clique em **Concluir**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Adicionar lógica para enviar o formulário, dependendo do estado conectado de um computador do usuário

1. No modo de design do InfoPath, clique em **Opções de envio** , na guia **dados** . 
    
2. Na caixa de diálogo **Opções de envio** , clique em **Permitir que os usuários enviem este formulário**, selecione **Executar ação personalizada usando o código**, clique em **Editar código**.
    
3. Adicione as seguintes duas funções abaixo o manipulador de eventos de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) : 
    
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

4. Adicione a seguinte instrução **se** para a função de manipulador de eventos de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) . 
    
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

1. No menu **Depurar** , clique em **Iniciar depuração**.
    
2. Preencha o formulário.
    
3. Inicie o Microsoft Internet Explorer.
    
4. No Internet Explorer, clique em **trabalhar offline** no menu **arquivo** . 
    
5. No InfoPath, clique em **Enviar**. Você deverá ver uma mensagem que o formulário será enviado como uma mensagem de email.
    
6. Clique em **Enviar**. Você verá uma mensagem informando que o formulário tiver sido enviado offline e será enviado ao se conectar à rede.
    
## <a name="see-also"></a>Confira também

- [Criar um modelo de formulário para uso offline](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)


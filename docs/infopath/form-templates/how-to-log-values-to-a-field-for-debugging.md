---
title: Valores de log para um campo de depuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Ao depurar um modelo de formulário do InfoPath, geralmente é útil registrar valores diretamente em um campo no formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431810"
---
# <a name="log-values-to-a-field-for-debugging"></a>Valores de log para um campo de depuração

Ao depurar um modelo de formulário do InfoPath, geralmente é útil registrar valores diretamente em um campo no formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.
  
## <a name="create-a-multi-line-text-field"></a>Criar um campo de texto de várias linhas

1. Adicione um **controle Caixa** de Texto ao formulário e reize-o para que ele possa exibir várias linhas. 
    
2. Clique com o botão direito do mouse na  caixa de texto, clique em **Propriedades** da Caixa de Texto e clique na caixa de seleção Várias Linhas na **guia** Exibir. 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Adicionar funções auxiliares para registrar informações de depuração no campo

1. Na guia **Desenvolvedor,** clique em **Editor de** Código e salve o modelo de formulário se for solicitado.
    
2. No Editor de Código, adicione as três funções auxiliares a seguir à classe pública no arquivo de código do formulário.
    
   > [!IMPORTANT]
   > Certifique-se de atualizar o valor definido para a variável na função para a expressão XPath correta para o campo vinculado ao controle que você criou  `debugFieldXpath`  `AddToDebugField` no primeiro procedimento. 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> Ao usar o Visual Basic, adicione  `Imports Microsoft.VisualBasic.Constants` às diretivas na parte superior do arquivo de código do formulário. 
  
## <a name="test-the-addtodebugfield-function"></a>Testar a função AddToDebugField

1. Na guia **Desenvolvedor,** clique em **Evento de** Carregamento e adicione a seguinte linha de código ao manipulador de eventos.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. Na guia **Desenvolvedor,** clique em Exibir Evento **Comutado** e adicione a seguinte linha de código ao manipulador de eventos.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. Na guia **Página** Home, clique em **Visualizar.**
    
   O campo de depuração deve exibir duas entradas: uma indicando que o formulário está carregado e outra indicando o nome do exibição. Esses exemplos usam manipuladores de eventos para eventos que ocorrem à medida que o formulário é aberto. No entanto, depois que o formulário é carregado, você pode chamar a função de outros manipuladores de eventos, além de qualquer outro código em execução no  `AddToDebugField` contexto do formulário. 
  


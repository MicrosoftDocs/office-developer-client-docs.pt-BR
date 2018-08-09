---
title: Valores de log para um campo para depuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Quando estiver depurando um modelo de formulário do InfoPath, geralmente é útil fazer logon valores diretamente em um campo do formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário. Os procedimentos a seguir mostram como criar um campo de várias linha e, em seguida, adicionar funções auxiliares para o código de formulário que permitem que você acesse os dados de depuração nesse campo.
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765621"
---
# <a name="log-values-to-a-field-for-debugging"></a>Valores de log para um campo para depuração

Quando estiver depurando um modelo de formulário do InfoPath, geralmente é útil fazer logon valores diretamente em um campo do formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário. Os procedimentos a seguir mostram como criar um campo de várias linha e, em seguida, adicionar funções auxiliares para o código de formulário que permitem que você acesse os dados de depuração nesse campo.
  
## <a name="create-a-multi-line-text-field"></a>Criar um campo de texto com várias linhas

1. Adicionar um controle de **Caixa de texto** para o formulário e, em seguida, redimensioná-lo para que ele possa exibir várias linhas. 
    
2. Com o botão direito na caixa de texto, clique em **Propriedades de caixa de texto**e, em seguida, clique em caixa de seleção **várias linhas** na guia **Exibir** . 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Adicionar funções auxiliares para registrar informações de depuração para o campo

1. Na guia **desenvolvedor** , clique em **Editor de código**e salve o modelo de formulário se você for solicitado.
    
2. No Editor de código, adicione as seguintes três funções de auxiliar à classe pública no arquivo de código de formulário.
    
   > [!IMPORTANT]
   > Certifique-se de que você atualizar o valor definido para o `debugFieldXpath` variável no `AddToDebugField` função para a expressão XPath correta para o campo vinculado ao controle que você criou no procedimento primeiro. 
  
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
> Quando usar o Visual Basic, adicione `Imports Microsoft.VisualBasic.Constants` às diretivas na parte superior do arquivo de código de formulário. 
  
## <a name="test-the-addtodebugfield-function"></a>Testar a função AddToDebugField

1. Na guia **desenvolvedor** , clique em **Carregar o evento**e, em seguida, adicione a seguinte linha de código para o manipulador de eventos.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. Na guia **desenvolvedor** , clique em **Exibir comutada evento**e, em seguida, adicione a seguinte linha de código para o manipulador de eventos.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. Na guia **página inicial** , clique em **Visualizar**.
    
   O campo de depuração deve exibir duas entradas: um indicando que o formulário é carregado e outro que indica o nome do modo de exibição. Estes exemplos usam manipuladores de eventos para os eventos que ocorrem conforme o formulário é aberto. No entanto, depois que o formulário é carregado, você pode chamar o `AddToDebugField` função de outros manipuladores de eventos, além de qualquer outro código em execução no contexto do formulário. 
  


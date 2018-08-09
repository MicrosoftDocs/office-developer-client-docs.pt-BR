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
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="bf555-104">Valores de log para um campo para depuração</span><span class="sxs-lookup"><span data-stu-id="bf555-104">Log values to a field for debugging</span></span>

<span data-ttu-id="bf555-105">Quando estiver depurando um modelo de formulário do InfoPath, geralmente é útil fazer logon valores diretamente em um campo do formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário.</span><span class="sxs-lookup"><span data-stu-id="bf555-105">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form.</span></span> <span data-ttu-id="bf555-106">Os procedimentos a seguir mostram como criar um campo de várias linha e, em seguida, adicionar funções auxiliares para o código de formulário que permitem que você acesse os dados de depuração nesse campo.</span><span class="sxs-lookup"><span data-stu-id="bf555-106">The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="bf555-107">Criar um campo de texto com várias linhas</span><span class="sxs-lookup"><span data-stu-id="bf555-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="bf555-108">Adicionar um controle de **Caixa de texto** para o formulário e, em seguida, redimensioná-lo para que ele possa exibir várias linhas.</span><span class="sxs-lookup"><span data-stu-id="bf555-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="bf555-109">Com o botão direito na caixa de texto, clique em **Propriedades de caixa de texto**e, em seguida, clique em caixa de seleção **várias linhas** na guia **Exibir** .</span><span class="sxs-lookup"><span data-stu-id="bf555-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="bf555-110">Adicionar funções auxiliares para registrar informações de depuração para o campo</span><span class="sxs-lookup"><span data-stu-id="bf555-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="bf555-111">Na guia **desenvolvedor** , clique em **Editor de código**e salve o modelo de formulário se você for solicitado.</span><span class="sxs-lookup"><span data-stu-id="bf555-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="bf555-112">No Editor de código, adicione as seguintes três funções de auxiliar à classe pública no arquivo de código de formulário.</span><span class="sxs-lookup"><span data-stu-id="bf555-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="bf555-113">Certifique-se de que você atualizar o valor definido para o `debugFieldXpath` variável no `AddToDebugField` função para a expressão XPath correta para o campo vinculado ao controle que você criou no procedimento primeiro.</span><span class="sxs-lookup"><span data-stu-id="bf555-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="bf555-114">Quando usar o Visual Basic, adicione `Imports Microsoft.VisualBasic.Constants` às diretivas na parte superior do arquivo de código de formulário.</span><span class="sxs-lookup"><span data-stu-id="bf555-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="bf555-115">Testar a função AddToDebugField</span><span class="sxs-lookup"><span data-stu-id="bf555-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="bf555-116">Na guia **desenvolvedor** , clique em **Carregar o evento**e, em seguida, adicione a seguinte linha de código para o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="bf555-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="bf555-117">Na guia **desenvolvedor** , clique em **Exibir comutada evento**e, em seguida, adicione a seguinte linha de código para o manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="bf555-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="bf555-118">Na guia **página inicial** , clique em **Visualizar**.</span><span class="sxs-lookup"><span data-stu-id="bf555-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="bf555-119">O campo de depuração deve exibir duas entradas: um indicando que o formulário é carregado e outro que indica o nome do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="bf555-119">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view.</span></span> <span data-ttu-id="bf555-120">Estes exemplos usam manipuladores de eventos para os eventos que ocorrem conforme o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="bf555-120">These examples use event handlers for events that occur as the form is opened.</span></span> <span data-ttu-id="bf555-121">No entanto, depois que o formulário é carregado, você pode chamar o `AddToDebugField` função de outros manipuladores de eventos, além de qualquer outro código em execução no contexto do formulário.</span><span class="sxs-lookup"><span data-stu-id="bf555-121">However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  


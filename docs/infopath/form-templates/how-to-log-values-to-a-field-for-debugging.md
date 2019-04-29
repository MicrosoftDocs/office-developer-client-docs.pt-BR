---
title: Valores de log para um campo de depuração
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Ao depurar um modelo de formulário do InfoPath, geralmente é útil registrar em log os valores diretamente em um campo no formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário. Os procedimentos a seguir mostram como criar um campo de várias linhas e, em seguida, adicionar funções auxiliares ao código de formulário que permite que você registre os dados de depuração nesse campo.
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431810"
---
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="9615b-104">Valores de log para um campo de depuração</span><span class="sxs-lookup"><span data-stu-id="9615b-104">Log values to a field for debugging</span></span>

<span data-ttu-id="9615b-105">Ao depurar um modelo de formulário do InfoPath, geralmente é útil registrar em log os valores diretamente em um campo no formulário para criar um registro de dados de depuração durante uma sessão de teste do formulário.</span><span class="sxs-lookup"><span data-stu-id="9615b-105">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form.</span></span> <span data-ttu-id="9615b-106">Os procedimentos a seguir mostram como criar um campo de várias linhas e, em seguida, adicionar funções auxiliares ao código de formulário que permite que você registre os dados de depuração nesse campo.</span><span class="sxs-lookup"><span data-stu-id="9615b-106">The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="9615b-107">Criar um campo de texto de várias linhas</span><span class="sxs-lookup"><span data-stu-id="9615b-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="9615b-108">Adicionar um controle de **caixa de texto** ao formulário e redimensioná-lo para que ele possa exibir várias linhas.</span><span class="sxs-lookup"><span data-stu-id="9615b-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="9615b-109">Clique com o botão direito do mouse na caixa de texto, clique em **Propriedades da caixa de texto**e clique na caixa de seleção de **várias linhas** na guia **Exibir** .</span><span class="sxs-lookup"><span data-stu-id="9615b-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="9615b-110">Adicionar funções auxiliares para registrar informações de depuração no campo</span><span class="sxs-lookup"><span data-stu-id="9615b-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="9615b-111">Na guia **desenvolvedor** , clique em **Editor de código**e salve o modelo de formulário, se for solicitado.</span><span class="sxs-lookup"><span data-stu-id="9615b-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="9615b-112">No editor de códigos, adicione as seguintes três funções auxiliares à classe pública no arquivo de código de formulário.</span><span class="sxs-lookup"><span data-stu-id="9615b-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="9615b-113">Verifique se você atualizou o valor definido para a `debugFieldXpath` variável na `AddToDebugField` função para a expressão XPath correta para o campo ligado ao controle que você criou no primeiro procedimento.</span><span class="sxs-lookup"><span data-stu-id="9615b-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="9615b-114">Ao usar o Visual Basic, `Imports Microsoft.VisualBasic.Constants` adicione às diretivas na parte superior do arquivo de código de formulário.</span><span class="sxs-lookup"><span data-stu-id="9615b-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="9615b-115">Testar a função AddToDebugField</span><span class="sxs-lookup"><span data-stu-id="9615b-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="9615b-116">Na guia **desenvolvedor** , clique em **carregar evento**e, em seguida, adicione a seguinte linha de código ao manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="9615b-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="9615b-117">Na guia **desenvolvedor** , clique em **Exibir evento alternado**e adicione a seguinte linha de código ao manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="9615b-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="9615b-118">Na guia **página inicial** , clique em **Visualização**.</span><span class="sxs-lookup"><span data-stu-id="9615b-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="9615b-119">O campo de depuração deve exibir duas entradas: uma indicando que o formulário está carregado e outro indicando o nome do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="9615b-119">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view.</span></span> <span data-ttu-id="9615b-120">Estes exemplos usam manipuladores de eventos para eventos que ocorrem quando o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="9615b-120">These examples use event handlers for events that occur as the form is opened.</span></span> <span data-ttu-id="9615b-121">No enTanto, após o carregamento do formulário, você pode `AddToDebugField` chamar a função de outros manipuladores de eventos, além de qualquer outro código em execução no contexto do formulário.</span><span class="sxs-lookup"><span data-stu-id="9615b-121">However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  


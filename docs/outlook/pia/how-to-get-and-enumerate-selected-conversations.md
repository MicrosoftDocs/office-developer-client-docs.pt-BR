---
title: Obter e enumerar conversas selecionadas
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320311"
---
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="b51d5-102">Obter e enumerar conversas selecionadas</span><span class="sxs-lookup"><span data-stu-id="b51d5-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="b51d5-103">Este exemplo obtém e enumera conversas escolhidas usando o método [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b51d5-103">This example obtains and enumerates selected conversations by using the [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="b51d5-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b51d5-104">Example</span></span>

<span data-ttu-id="b51d5-105">O Microsoft Outlook pode ser definido para exibir itens na caixa de entrada por conversa.</span><span class="sxs-lookup"><span data-stu-id="b51d5-105">Microsoft Outlook can be set to display items in the Inbox by conversation.</span></span> <span data-ttu-id="b51d5-106">Se um usuário marcar algum item na Caixa de Entrada, é possível ter acesso a essa seleção programaticamente, incluindo cabeçalhos de conversas e itens de conversa.</span><span class="sxs-lookup"><span data-stu-id="b51d5-106">If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items.</span></span> <span data-ttu-id="b51d5-107">O exemplo de código neste tópico mostra como ter acesso à seleção na Caixa de Entrada e enumerar os itens de email em cada conversa na seleção.</span><span class="sxs-lookup"><span data-stu-id="b51d5-107">The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.</span></span>

<span data-ttu-id="b51d5-108">O exemplo contém um método DemoConversationHeadersFromSelection.</span><span class="sxs-lookup"><span data-stu-id="b51d5-108">The example contains one method, DemoConversationHeadersFromSelection.</span></span> <span data-ttu-id="b51d5-109">O método define a exibição atual para a Caixa de Entrada e, em seguida, verifica se a exibição atual é uma exibição de tabela que exibe conversas ordenadas por data.</span><span class="sxs-lookup"><span data-stu-id="b51d5-109">The method sets the current view to the Inbox, and then checks whether the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="b51d5-110">Para obter uma seleção, incluindo quaisquer objetos [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) escolhidos, DemoConversationHeadersFromSelection usa o método **GetSelection** do objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) especificando a constante [olConversionHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) como um argumento.</span><span class="sxs-lookup"><span data-stu-id="b51d5-110">To obtain a selection, including any selected [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) objects, DemoConversationHeadersFromSelection uses the **GetSelection** method of the [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object, specifying the [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) constant as an argument.</span></span> <span data-ttu-id="b51d5-111">Se cabeçalhos de conversa forem marcados, DemoConversationHeadersFromSelection usa o objeto [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) para enumerar itens em cada conversa marcada e, em seguida, exibe o assunto desses itens de conversa que são objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b51d5-111">If conversation headers are selected, DemoConversationHeadersFromSelection uses the [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) object to enumerate items in each selected conversation, and then displays the subject of those conversation items that are [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects.</span></span>

<span data-ttu-id="b51d5-112">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b51d5-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b51d5-113">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="b51d5-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b51d5-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="b51d5-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b51d5-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b51d5-115">See also</span></span>

- [<span data-ttu-id="b51d5-116">Conversas</span><span class="sxs-lookup"><span data-stu-id="b51d5-116">Conversations</span></span>](conversations.md)


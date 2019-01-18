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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699370"
---
# <a name="get-and-enumerate-selected-conversations"></a>Obter e enumerar conversas selecionadas

Este exemplo obtém e enumera conversas escolhidas usando o método [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)).

## <a name="example"></a>Exemplo

O Microsoft Outlook pode ser definido para exibir itens na caixa de entrada por conversa. Se um usuário marcar algum item na Caixa de Entrada, é possível ter acesso a essa seleção programaticamente, incluindo cabeçalhos de conversas e itens de conversa. O exemplo de código neste tópico mostra como ter acesso à seleção na Caixa de Entrada e enumerar os itens de email em cada conversa na seleção.

O exemplo contém um método DemoConversationHeadersFromSelection. O método define a exibição atual para a Caixa de Entrada e, em seguida, verifica se a exibição atual é uma exibição de tabela que exibe conversas ordenadas por data. Para obter uma seleção, incluindo quaisquer objetos [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) escolhidos, DemoConversationHeadersFromSelection usa o método **GetSelection** do objeto [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) especificando a constante [olConversionHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) como um argumento. Se cabeçalhos de conversa forem marcados, DemoConversationHeadersFromSelection usa o objeto [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) para enumerar itens em cada conversa marcada e, em seguida, exibe o assunto desses itens de conversa que são objetos [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Conversas](conversations.md)


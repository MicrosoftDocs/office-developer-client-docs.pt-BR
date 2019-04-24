---
title: Obter e exibir itens em uma conversa
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fcfe76632c2fda742a85a571d655569dc2fcd33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349459"
---
# <a name="get-and-display-items-in-a-conversation"></a>Obter e exibir itens em uma conversa

Este exemplo mostra como obter e exibir itens de email em uma conversa.

## <a name="example"></a>Exemplo

No exemplo de código a seguir, DemoConversation obtém um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e, em seguida, determina o armazenamento do objeto **MailItem** usando a propriedade [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) do objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)). DemoConversation verifica se a propriedade [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) é **true**; se for **true**, o exemplo de código obtém o objeto [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) usando o método [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)). Se o objeto **Conversation** não for uma referência nula, o exemplo obtém o objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) associado que contém cada item na conversa usando o método [GetTable ()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)). 

O exemplo, em seguida, enumera cada item na **Table** e chama EnumerateConversation em cada item para acessar os nós filhos de cada item. EnumerateConversation usa um objeto **Conversation** e obtém os nós filhos usando o método [GetChildren (Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)). EnumerateConversation é chamado recursivamente até que não haja mais nós filho. Cada item de conversa é exibido ao usuário.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Conversas](conversations.md)


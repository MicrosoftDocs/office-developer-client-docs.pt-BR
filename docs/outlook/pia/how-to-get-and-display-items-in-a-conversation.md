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
# <a name="get-and-display-items-in-a-conversation"></a><span data-ttu-id="c956d-102">Obter e exibir itens em uma conversa</span><span class="sxs-lookup"><span data-stu-id="c956d-102">Get and display items in a conversation</span></span>

<span data-ttu-id="c956d-103">Este exemplo mostra como obter e exibir itens de email em uma conversa.</span><span class="sxs-lookup"><span data-stu-id="c956d-103">This example shows how to get and display mail items in a conversation.</span></span>

## <a name="example"></a><span data-ttu-id="c956d-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c956d-104">Example</span></span>

<span data-ttu-id="c956d-105">No exemplo de código a seguir, DemoConversation obtém um objeto [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) e, em seguida, determina o armazenamento do objeto **MailItem** usando a propriedade [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) do objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c956d-105">In the following code example, DemoConversation gets a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and then determines the store of the **MailItem** object by using the [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) property of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span> <span data-ttu-id="c956d-106">DemoConversation verifica se a propriedade [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) é **true**; se for **true**, o exemplo de código obtém o objeto [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) usando o método [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c956d-106">DemoConversation then checks whether the [IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) property is **true**; if it is **true**, the code example gets [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) object by using the [GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)) method.</span></span> <span data-ttu-id="c956d-107">Se o objeto **Conversation** não for uma referência nula, o exemplo obtém o objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) associado que contém cada item na conversa usando o método [GetTable ()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c956d-107">If the **Conversation** object is not a null reference, the example gets the associated [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains each item in the conversation by using the [GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)) method.</span></span> 

<span data-ttu-id="c956d-108">O exemplo, em seguida, enumera cada item na **Table** e chama EnumerateConversation em cada item para acessar os nós filhos de cada item.</span><span class="sxs-lookup"><span data-stu-id="c956d-108">The example then enumerates each item in the **Table** and calls EnumerateConversation on each item to access the child nodes of each item.</span></span> <span data-ttu-id="c956d-109">EnumerateConversation usa um objeto **Conversation** e obtém os nós filhos usando o método [GetChildren (Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c956d-109">EnumerateConversation takes a **Conversation** object and gets the child nodes by using the [GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)) method.</span></span> <span data-ttu-id="c956d-110">EnumerateConversation é chamado recursivamente até que não haja mais nós filho.</span><span class="sxs-lookup"><span data-stu-id="c956d-110">EnumerateConversation is called recursively until there are no more child nodes.</span></span> <span data-ttu-id="c956d-111">Cada item de conversa é exibido ao usuário.</span><span class="sxs-lookup"><span data-stu-id="c956d-111">Each conversation item is then displayed to the user.</span></span>

<span data-ttu-id="c956d-112">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c956d-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c956d-113">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="c956d-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c956d-114">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="c956d-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c956d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c956d-115">See also</span></span>

- [<span data-ttu-id="c956d-116">Conversas</span><span class="sxs-lookup"><span data-stu-id="c956d-116">Conversations</span></span>](conversations.md)


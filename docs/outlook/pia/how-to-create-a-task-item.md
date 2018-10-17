---
title: Criar um item de tarefa
TOCTitle: Create a task item
ms:assetid: d458dd31-2771-4a3c-a713-13c7e4e02a74
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184644(v=office.15)
ms:contentKeyID: 55119894
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 467d715e0fca1adfd835b11c36889dff3dbf145d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406803"
---
# <a name="create-a-task-item"></a><span data-ttu-id="08935-102">Criar um item de tarefa</span><span class="sxs-lookup"><span data-stu-id="08935-102">Create a task.</span></span>

<span data-ttu-id="08935-103">Este exemplo mostra como criar um item de tarefa usando o método [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="08935-103">This example shows how to create a task item by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="08935-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="08935-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="08935-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="08935-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="08935-106">No exemplo de código a seguir, CreateToDoItemExample cria um item de tarefa pendente chamando o método **MarkAsTask** no item e salvando o item.</span><span class="sxs-lookup"><span data-stu-id="08935-106">In the following code example, CreateToDoItemExample creates a to-do item by calling the **MarkAsTask** method on the item and then saving the item.</span></span> <span data-ttu-id="08935-107">O exemplo marca o item para acompanhamento amanhã e define um lembrete para amanhã às 10h00</span><span class="sxs-lookup"><span data-stu-id="08935-107">The example marks the item for follow-up tomorrow and sets a reminder for tomorrow at 10:00 A.M.</span></span> <span data-ttu-id="08935-108">usando as propriedades [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) e [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="08935-108">by using the [ReminderSet](https://msdn.microsoft.com/library/bb622600\(v=office.15\)) and [ReminderTime](https://msdn.microsoft.com/library/bb622803\(v=office.15\)) properties.</span></span> <span data-ttu-id="08935-109">Em seguida, o exemplo usa o método [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) para salvar o item.</span><span class="sxs-lookup"><span data-stu-id="08935-109">The example then uses the [Save()](https://msdn.microsoft.com/library/bb645518\(v=office.15\)) method to save the item.</span></span>

<span data-ttu-id="08935-110">Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="08935-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="08935-111">A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública.</span><span class="sxs-lookup"><span data-stu-id="08935-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="08935-112">A seguinte linha de código mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="08935-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateToDoItemExample()
{
    // Date operations
    DateTime today = DateTime.Parse("10:00 AM");
    TimeSpan duration = TimeSpan.FromDays(1);
    DateTime tomorrow = today.Add(duration);
    Outlook.MailItem mail = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Find(
        "[MessageClass]='IPM.Note'") as Outlook.MailItem;
    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkTomorrow);
    mail.TaskStartDate = today;
    mail.ReminderSet = true;
    mail.ReminderTime = tomorrow;
    mail.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="08935-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="08935-113">See also</span></span>

- [<span data-ttu-id="08935-114">Tarefas</span><span class="sxs-lookup"><span data-stu-id="08935-114">Tasks</span></span>](tasks.md)


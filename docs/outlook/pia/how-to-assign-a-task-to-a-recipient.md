---
title: Atribuir uma tarefa a um destinatário
TOCTitle: Assign a task to a recipient
ms:assetid: c6be97a7-de3f-43e5-9111-534d0f04e986
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184639(v=office.15)
ms:contentKeyID: 55119929
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54259b00fb3eb67c86985758bb86f5ab7ba120eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359730"
---
# <a name="assign-a-task-to-a-recipient"></a><span data-ttu-id="d051a-102">Atribuir uma tarefa a um destinatário</span><span class="sxs-lookup"><span data-stu-id="d051a-102">Assign a task to a recipient</span></span>

<span data-ttu-id="d051a-103">O exemplo a seguir mostra como criar e atribuir uma tarefa a um destinatário.</span><span class="sxs-lookup"><span data-stu-id="d051a-103">This example shows how to create a task and assign it to a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="d051a-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d051a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="d051a-105">O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="d051a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="d051a-106">No exemplo a seguir, AssignTaskExample cria um objeto [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) e especifica os valores para as propriedades [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)) e [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="d051a-106">In the following code example, AssignTaskExample creates a [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object and specifies values for the [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)), and [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)) properties.</span></span> <span data-ttu-id="d051a-107">O método [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) especifica que esta é uma tarefa atribuída.</span><span class="sxs-lookup"><span data-stu-id="d051a-107">The [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) method specifies that the task is an assigned task.</span></span> <span data-ttu-id="d051a-108">Após a adição de um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a **TaskItem** usando o método [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)), o método [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) envia a tarefa para o destinatário.</span><span class="sxs-lookup"><span data-stu-id="d051a-108">After a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object is added to the **TaskItem** by using the [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method, the [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) method sends the task to the recipient.</span></span>

<span data-ttu-id="d051a-109">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="d051a-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="d051a-110">A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública.</span><span class="sxs-lookup"><span data-stu-id="d051a-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="d051a-111">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="d051a-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AssignTaskExample()
{
    Outlook.TaskItem task = Application.CreateItem(
        Outlook.OlItemType.olTaskItem) as Outlook.TaskItem;
    task.Subject = "Tax Preparation";
    task.StartDate = DateTime.Parse("4/1/2007 8:00 AM");
    task.DueDate = DateTime.Parse("4/15/2007 8:00 AM");
    Outlook.RecurrencePattern pattern =
        task.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearly;
    pattern.PatternStartDate = DateTime.Parse("4/1/2007");
    pattern.NoEndDate = true;
    task.ReminderSet = true;
    task.ReminderTime = DateTime.Parse("4/1/2007 8:00 AM");
    task.Assign();
    task.Recipients.Add("accountant@example.com");
    task.Recipients.ResolveAll();
    task.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="d051a-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="d051a-112">See also</span></span>

- [<span data-ttu-id="d051a-113">Tarefas</span><span class="sxs-lookup"><span data-stu-id="d051a-113">Tasks</span></span>](tasks.md)


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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726096"
---
# <a name="assign-a-task-to-a-recipient"></a>Atribuir uma tarefa a um destinatário

O exemplo a seguir mostra como criar e atribuir uma tarefa a um destinatário.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


No exemplo a seguir, AssignTaskExample cria um objeto [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) e especifica os valores para as propriedades [Subject](https://msdn.microsoft.com/library/bb624148\(v=office.15\)), [StartDate](https://msdn.microsoft.com/library/bb643988\(v=office.15\)) e [DueDate](https://msdn.microsoft.com/library/bb612307\(v=office.15\)). O método [Assign()](https://msdn.microsoft.com/library/bb644565\(v=office.15\)) especifica que esta é uma tarefa atribuída. Após a adição de um objeto [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) a **TaskItem** usando o método [Add(String)](https://msdn.microsoft.com/library/bb612668\(v=office.15\)), o método [Send()](https://msdn.microsoft.com/library/bb646608\(v=office.15\)) envia a tarefa para o destinatário.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. A seguinte linha de código mostra como fazer a importação e atribuição em C\#.

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

## <a name="see-also"></a>Confira também

- [Tarefas](tasks.md)


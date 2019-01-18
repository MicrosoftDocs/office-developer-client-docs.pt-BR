---
title: Responder a um item de solicitação de tarefa
TOCTitle: Respond to a task request item
ms:assetid: 573c98ef-4d15-4fd1-bccd-25a22c9a63f0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184608(v=office.15)
ms:contentKeyID: 55119896
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9aa6416680bbf2443506415b5fa871d30fe5f32e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705404"
---
# <a name="respond-to-a-task-request-item"></a>Responder a um item de solicitação de tarefa

Este exemplo mostra como obter e responder um item de solicitação de tarefa.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo a seguir, AcceptTaskRequest usa o método [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) do objeto [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) para obter o objeto [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)). O exemplo chama o método [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)) com o parâmetro definido como [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)) para aceitar a solicitação de tarefa.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. A seguinte linha de código mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AcceptTaskRequest()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).
        Items.Restrict(filter);
    if (items.Count > 0)
    {
        Outlook.TaskRequestItem taskRequest =
            (Outlook.TaskRequestItem)items[1];
        Outlook.TaskItem task =
            taskRequest.GetAssociatedTask(false);
        Outlook.TaskItem taskResponse = task.Respond(
            Outlook.OlTaskResponse.olTaskAccept, true, false);
        taskResponse.Send();
    }
}
```

## <a name="see-also"></a>Confira também

- [Tarefas](tasks.md)


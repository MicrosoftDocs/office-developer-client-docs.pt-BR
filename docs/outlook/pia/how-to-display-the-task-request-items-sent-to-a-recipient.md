---
title: Exibir os itens de solicitação de tarefas enviados para um destinatário
TOCTitle: Display the task request items sent to a recipient
ms:assetid: 167c3d52-67b5-467c-a7b6-e8cc96002b63
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184591(v=office.15)
ms:contentKeyID: 55119930
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9ab5e830003fbfb64b44fc9e0d813c7a7c5163bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357418"
---
# <a name="display-the-task-request-items-sent-to-a-recipient"></a>Exibir os itens de solicitação de tarefas enviados para um destinatário

Este exemplo mostra como exibir todos os itens da solicitação de tarefas que estão na Caixa de Entrada de um destinatário.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um objeto [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) representa uma solicitação para atribuir uma tarefa a outro usuário. O **TaskRequestItem** é criado quando o item é recebido na Caixa de Entrada do destinatário. No exemplo de código a seguir, ShowTaskRequests filtra a Caixa de Entrada de um destinatário, cria um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) e insere uma linha para cada item para o qual o valor da propriedade [MessageClass](https://msdn.microsoft.com/library/bb610592\(v=office.15\)) é igual a **IPM.TaskRequest**. O assunto de cada tarefa na pasta Caixa de Entrada do destinatário é então gravado nos ouvintes de rastreamento do conjunto [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowTaskRequests()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).GetTable
        (filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>Confira também

- [Tarefas](tasks.md)


---
title: Enumerar itens em um modo de exibição de tabela
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3bde66fd07a39aa8a63219876b9bdbcf72e00f7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717675"
---
# <a name="enumerate-items-in-a-table-view"></a>Enumerar itens em um modo de exibição de tabela

Este exemplo enumera itens em um modo de exibição de tabela usando o método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)).

## <a name="example"></a>Exemplo

O exemplo de código a seguir obtém um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) do modo de exibição atual da pasta Caixa de Entrada. O exemplo de código define a pasta atual do explorador ativo à Caixa de Entrada e, em seguida, verifica se o modo de exibição atual da Caixa de Entrada é um modo de exibição de tabela. Se o modo de exibição atual for uma tabela, o exemplo de código chamará o método [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) e exibirá cada item representado por cada linha no objeto **Table** retornado.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução **using** não deve vir diretamente antes de funções no exemplo de código, mas deve ser adicionada antes da declaração Class pública. A seguinte linha de código mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Modos de exibição](views.md)


---
title: Enumerar itens ocultos em uma pasta
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b048ec7fb47a8cbf6b8b49115c59079754fd4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406019"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>Enumerar itens ocultos em uma pasta

Este exemplo mostra como localizar e enumerar itens ocultos em uma pasta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Um recurso do objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)), que representa um conjunto de itens em uma pasta, é que ele pode ter itens ocultos. Para retornar itens ocultos em uma pasta, defina o parâmetro *TableContents* no método [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) do objeto [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) para [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)). No exemplo de código a seguir, TableForInboxHiddenItems obtém os itens ocultos de uma pasta Caixa de Entrada e grava os valores das propriedades [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) e [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) de cada item oculto nos ouvintes de rastreamento da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a>Confira também

-[Pesquisar e filtrar](search-and-filter.md)


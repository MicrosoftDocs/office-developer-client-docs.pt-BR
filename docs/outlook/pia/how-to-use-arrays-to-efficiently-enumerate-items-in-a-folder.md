---
title: Usar matrizes para enumerar itens em uma pasta com eficiência
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d165b27da58a4e99eabb897aac3d2dc03811f588
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407503"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>Usar matrizes para enumerar itens em uma pasta com eficiência

Este exemplo mostra como enumerar com eficiência itens em um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) usando o método [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)).

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir foi tirado do artigo [Programação de aplicativos do Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

No exemplo de código a seguir, DemoGetArrayForTable obtém um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) de um objeto **Folder** usando o método [GetTable (Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)). DemoGetArrayForTable então usa o método **GetArray** para retornar um objeto [Array](https://msdn.microsoft.com/library/system.array.aspx) que contém elementos para cada linha da tabela. O objeto **Array** retornado é uma matriz bidimensional que representa um conjunto de valores de linha e coluna da **Table**. A matriz é baseada em zero, em vez de baseada em um, como é o caso de coleções do Outlook. Uma vez obtido o objeto **Array**, o código usa um loop for para enumerar por meio da tabela.

Se você usar o Visual Studio para testar este exemplo de código, primeiro adicione uma referência para o componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável Outlook ao importar o namespace **Microsoft.Office.Interop.Outlook**. A instrução**using** não deve ocorrer diretamente antes das funções no exemplo de código, mas deve ser adicionada antes da declaração de classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)


---
title: Filtrar e exibir propriedades de valores múltiplos ao enumerar itens em uma pasta
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: acb6f6807f956ee6d468d3fcefc2cdd27732ab9b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726404"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a>Filtrar e exibir propriedades de valores múltiplos ao enumerar itens em uma pasta

Este exemplo mostra como filtrar e exibir propriedade de valores múltiplos ao enumerar itens em uma pasta.

## <a name="example"></a>Exemplo

> [!NOTE] 
> O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de dados de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)). Quando um binário, data ou propriedade de valores múltiplos é adicionada primeiro a um objeto **Table**, a maneira como a propriedade é referenciada afeta seu tipo e formato. Em razão das referências de nome internas algumas vezes retornarem um valor de coluna diferente da referência namespace, você deve determinar se a propriedade é referenciada por seu nome interno explícito (se houver um) ou por um namespace (sem importar a existência de um nome interno explícito). A tabela a seguir mostra a diferença na representação do valor de propriedade (em termos de tipo e formato) segundo o tipo de propriedade original.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo</p></th>
<th><p>Retorna o tipo se a propriedade especificada usar um nome interno</p></th>
<th><p>Retorna o tipo se a propriedade especificada usar um namespace</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Binário <b>(PT_BINARY)</b></p></td>
<td><p>String</p></td>
<td><p>Matriz de bytes</p></td>
</tr>
<tr class="even">
<td><p>Data <b>(PT_SYSTIME)</b></p></td>
<td><p>Local <b>DateTime</b></p></td>
<td><p>UTC <b>DateTime</b></p></td>
</tr>
<tr class="odd">
<td><p>Múltiplos valores (também conhecido como o tipo de palavra-chave), como a propriedade <b>Categories</b><b>(PT_MV_STRING8)</b></p></td>
<td><p>Cadeia de caracteres contendo valores separados por vírgula</p></td>
<td><p>Matriz unidimensional que contém um elemento para cada palavra-chave</p></td>
</tr>
</tbody>
</table>


O exemplo de código a seguir ilustra como adicionar uma propriedade de namespace de cadeia de caracteres MAPI ao objeto **Table** e como propriedades de valores múltiplos afetam os valores retornados em um objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)). O procedimento TableMultiValuedProperties filtra o objeto **Table** para linhas onde a propriedade [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) não é uma referência nula. A propriedade **Categories** é representada por uma propriedade que uma o namespace da cadeia de caracteres MAPI. Um filtro DAV Searching and Locating (DASL) é construído para itens que têm categorias (o filtro real retorna categorias que não têm uma referência nula). Então, a coluna **Categories** é adicionada ao objeto **Table** concatenando-se o especificador de tipos, 0000001f, com a constante categoriesProperty. Por fim, o objeto **Column** que representa a propriedade **Categories** contém uma matriz de cadeia unidimensional, onde cada elemento da matriz representa uma categoria atribuída ao item. As duas propriedades do item **Categories** e **Subject** são escritas para os ouvintes de rastreamento da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Se usar o Visual Studio para testas este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**. O ** que usa a instrução** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública. A linha de código seguinte mostra como fazer a importação e atribuição em C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableMultiValuedProperties()
{
    const string categoriesProperty =
        "https://schemas.microsoft.com/mapi/string/"
        + "{00020329-0000-0000-C000-000000000046}/Keywords";
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with filter for categories
    string filter = "@SQL="
        + "Not(" + "\"" + categoriesProperty
        + "\"" + " Is Null)";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Add categories column and append type specifier
    table.Columns.Add(categoriesProperty + "/0000001F");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        string[] categories =
            (string[])nextRow[categoriesProperty + "/0000001F"];
        Debug.WriteLine("Subject: " + nextRow["Subject"]);
        Debug.Write("Categories: ");
        foreach (string category in categories)
        {
            Debug.Write("\t" + category);
        }
        Debug.WriteLine("\n");
    }
}
```

## <a name="see-also"></a>Confira também

- [Pesquisar e filtrar](search-and-filter.md)


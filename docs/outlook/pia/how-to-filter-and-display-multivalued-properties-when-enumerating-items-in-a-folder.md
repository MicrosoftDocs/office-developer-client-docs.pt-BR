---
title: Filtrar e exibir propriedades de valores múltiplos ao enumerar itens em uma pasta
TOCTitle: Filter and display multivalued properties when enumerating items in a folder
ms:assetid: 62dd2120-5c85-44b3-89ec-c4ca85aa2964
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184613(v=office.15)
ms:contentKeyID: 55119887
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: bb1abdeb97e15225e77f9e04a4c34e91e70a533a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407454"
---
# <a name="filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="76982-102">Filtrar e exibir propriedades de valores múltiplos ao enumerar itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="76982-102">Filter and display multivalued properties when enumerating items in a folder</span></span>

<span data-ttu-id="76982-103">Este exemplo mostra como filtrar e exibir propriedade de valores múltiplos ao enumerar itens em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="76982-103">This example shows how to filter and display multivalued properties while enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="76982-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76982-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="76982-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="76982-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="76982-106">O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de dados de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="76982-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="76982-107">Quando um binário, data ou propriedade de valores múltiplos é adicionada primeiro a um objeto **Table**, a maneira como a propriedade é referenciada afeta seu tipo e formato.</span><span class="sxs-lookup"><span data-stu-id="76982-107">When a binary, date, or multivalued property is first added to a **Table** object, the way the property is referenced affects its type and format.</span></span> <span data-ttu-id="76982-108">Em razão das referências de nome internas algumas vezes retornarem um valor de coluna diferente da referência namespace, você deve determinar se a propriedade é referenciada por seu nome interno explícito (se houver um) ou por um namespace (sem importar a existência de um nome interno explícito).</span><span class="sxs-lookup"><span data-stu-id="76982-108">Because built-in name references sometimes return a different column value than a namespace reference, you should determine whether the property is referenced by its explicit built-in name (if it has one), or by namespace (regardless of the existence of an explicit built-in name).</span></span> <span data-ttu-id="76982-109">A tabela a seguir mostra a diferença na representação do valor de propriedade (em termos de tipo e formato) segundo o tipo de propriedade original.</span><span class="sxs-lookup"><span data-stu-id="76982-109">The following table summarizes the difference in the property value representation (in terms of type and format) per original property type:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76982-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="76982-110">Type</span></span></p></th>
<th><p><span data-ttu-id="76982-111">Retorna o tipo se a propriedade especificada usar um nome interno</span><span class="sxs-lookup"><span data-stu-id="76982-111">Return type if the specified property uses a built-in name</span></span></p></th>
<th><p><span data-ttu-id="76982-112">Retorna o tipo se a propriedade especificada usar um namespace</span><span class="sxs-lookup"><span data-stu-id="76982-112">Return type if the specified property uses a namespace</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76982-113">Binário <b>(PT_BINARY)</b></span><span class="sxs-lookup"><span data-stu-id="76982-113">Binary <b>(PT_BINARY)</b></span></span></p></td>
<td><p><span data-ttu-id="76982-114">String</span><span class="sxs-lookup"><span data-stu-id="76982-114">String</span></span></p></td>
<td><p><span data-ttu-id="76982-115">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="76982-115">Byte array</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76982-116">Data <b>(PT_SYSTIME)</b></span><span class="sxs-lookup"><span data-stu-id="76982-116">Date <b>(PT_SYSTIME)</b></span></span></p></td>
<td><p><span data-ttu-id="76982-117">Local <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="76982-117">Local <b>DateTime</b></span></span></p></td>
<td><p><span data-ttu-id="76982-118">UTC <b>DateTime</b></span><span class="sxs-lookup"><span data-stu-id="76982-118">UTC <b>DateTime</b></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76982-119">Múltiplos valores (também conhecido como o tipo de palavra-chave), como a propriedade <b>Categories</b><b>(PT_MV_STRING8)</b></span><span class="sxs-lookup"><span data-stu-id="76982-119">Multivalued (also known as keyword type) such as <b>Categories</b> property <b>(PT_MV_STRING8)</b></span></span></p></td>
<td><p><span data-ttu-id="76982-120">Cadeia de caracteres contendo valores separados por vírgula</span><span class="sxs-lookup"><span data-stu-id="76982-120">String that contains comma-separated values</span></span></p></td>
<td><p><span data-ttu-id="76982-121">Matriz unidimensional que contém um elemento para cada palavra-chave</span><span class="sxs-lookup"><span data-stu-id="76982-121">One-dimensional array that contains one element for each keyword</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="76982-122">O exemplo de código a seguir ilustra como adicionar uma propriedade de namespace de cadeia de caracteres MAPI ao objeto **Table** e como propriedades de valores múltiplos afetam os valores retornados em um objeto [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="76982-122">The following code example illustrates how to add a MAPI string namespace property to the **Table** object and how multivalued properties affect the values returned in a [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object.</span></span> <span data-ttu-id="76982-123">O procedimento TableMultiValuedProperties filtra o objeto **Table** para linhas onde a propriedade [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) não é uma referência nula.</span><span class="sxs-lookup"><span data-stu-id="76982-123">The TableMultiValuedProperties procedure filters the **Table** object for rows where the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) property is not a null reference.</span></span> <span data-ttu-id="76982-124">A propriedade **Categories** é representada por uma propriedade que uma o namespace da cadeia de caracteres MAPI.</span><span class="sxs-lookup"><span data-stu-id="76982-124">The **Categories** property is represented by a property that uses the MAPI string namespace.</span></span> <span data-ttu-id="76982-125">Um filtro DAV Searching and Locating (DASL) é construído para itens que têm categorias (o filtro real retorna categorias que não têm uma referência nula).</span><span class="sxs-lookup"><span data-stu-id="76982-125">A DAV Searching and Locating (DASL) filter is constructed for items that have categories (the actual filter returns categories that do not have a null reference).</span></span> <span data-ttu-id="76982-126">Então, a coluna **Categories** é adicionada ao objeto **Table** concatenando-se o especificador de tipos, 0000001f, com a constante categoriesProperty.</span><span class="sxs-lookup"><span data-stu-id="76982-126">A **Categories** column is then added to the **Table** object by concatenating the type specifier, 0000001f, with the categoriesProperty constant.</span></span> <span data-ttu-id="76982-127">Por fim, o objeto **Column** que representa a propriedade **Categories** contém uma matriz de cadeia unidimensional, onde cada elemento da matriz representa uma categoria atribuída ao item.</span><span class="sxs-lookup"><span data-stu-id="76982-127">Finally, the **Column** object that represents the **Categories** property contains a one-dimensional string array where each element of the array represents a category assigned to the item.</span></span> <span data-ttu-id="76982-128">As duas propriedades do item **Categories** e **Subject** são escritas para os ouvintes de rastreamento da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="76982-128">Both the item’s **Categories** and **Subject** properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="76982-129">Se usar o Visual Studio para testas este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="76982-129">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="76982-130">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="76982-130">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="76982-131">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="76982-131">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="76982-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="76982-132">See also</span></span>

- [<span data-ttu-id="76982-133">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="76982-133">Search and Filter</span></span>](search-and-filter.md)


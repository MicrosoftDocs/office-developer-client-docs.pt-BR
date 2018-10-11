---
title: Filtrar e enumerar itens em uma pasta de forma eficiente
TOCTitle: Filter and efficiently enumerate items in a folder
ms:assetid: efee7704-b7d9-4586-a72e-4e960ec1ffdb
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612664(v=office.15)
ms:contentKeyID: 55119884
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01f0019d0f038cd1e9ea8fee7c85d0d2f18c4b47
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405669"
---
# <a name="filter-and-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="acdd9-102">Filtrar e enumerar itens em uma pasta de forma eficiente</span><span class="sxs-lookup"><span data-stu-id="acdd9-102">Filter and efficiently enumerate items in a folder</span></span>

<span data-ttu-id="acdd9-103">Este exemplo mostra como usar o objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) para filtrar itens na Caixa de Entrada que tenham anexos e enumerá-los de forma eficiente, exibindo as propriedades selecionadas para cada item.</span><span class="sxs-lookup"><span data-stu-id="acdd9-103">This example shows how to use the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object to filter for items in the Inbox that have attachments, and efficiently enumerate such items, displaying selected properties for each item.</span></span>

## <a name="example"></a><span data-ttu-id="acdd9-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="acdd9-104">Example</span></span>

<span data-ttu-id="acdd9-105">O código de exemplo especifica a propriedade **PR\_HASATTACH** com o namespace MAPI e usa a propriedade para criar o filtro inicial no método [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) na Caixa de Entrada.</span><span class="sxs-lookup"><span data-stu-id="acdd9-105">The code sample specifies the property **PR\_HASATTACH** with the MAPI namespace, and uses the property to create the initial filter in the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox.</span></span> <span data-ttu-id="acdd9-106">Um objeto **Table** para um tipo de item tem colunas padrão representando certas propriedades desse tipo de item.</span><span class="sxs-lookup"><span data-stu-id="acdd9-106">A **Table** object for an item type has default columns representing certain properties of that item type.</span></span> <span data-ttu-id="acdd9-107">Para personalizar as colunas, este exemplo primeiro chama o método [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) no conjunto [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) desse **Table** e chama o método [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) no conjunto **Columns** para adicionar as propriedades **EntryID**, **Subject** e **ReceivedTime** usando os nomes de propriedade internos, com a coluna **ReceivedTime** armazenando valores na representação local de data e hora.</span><span class="sxs-lookup"><span data-stu-id="acdd9-107">To customize the columns, this example first calls the [RemoveAll](https://msdn.microsoft.com/library/bb611528\(v=office.15\)) method on the [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) collection of that **Table**, and then calls the [Add](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method on the **Columns** collection to add the **EntryID**, **Subject**, and **ReceivedTime** properties using the built-in property names, with the **ReceivedTime** column storing values in local date-time representation.</span></span> 

<span data-ttu-id="acdd9-108">O exemplo então chama **Columns.Add** mais uma vez para adicionar a propriedade **ReceiveTime** especificando seu namespace MAPI, para que esta coluna armazene o valor como um valor de data e hora no Tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="acdd9-108">The example then calls **Columns.Add** one more time to add the **ReceiveTime** property specifying its MAPI namespace so that this column will store the value as a Universal Coordinated Time (UTC) date-time value.</span></span> <span data-ttu-id="acdd9-109">Por fim, o exemplo enumera cada item na tabela, mostrando o valor de cada uma das quatro propriedades especificadas como as colunas da tabela.</span><span class="sxs-lookup"><span data-stu-id="acdd9-109">Finally, the example enumerates each item in the Table, displaying the value of each of the four properties specified as the table columns.</span></span>

<span data-ttu-id="acdd9-110">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="acdd9-110">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="acdd9-111">A instrução **Imports** ou **using** não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionada antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="acdd9-111">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="acdd9-112">As seguintes linhas de código mostram como fazer a importação e atribuição de tarefas em Visual Basic e C\#.</span><span class="sxs-lookup"><span data-stu-id="acdd9-112">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoTableColumns()
    Const PR_HAS_ATTACH As String = _
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B"
    ' Obtain Inbox
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox), _
        Outlook.Folder)
    ' Create filter
    Dim filter As String = "@SQL=" & Chr(34) _
        & PR_HAS_ATTACH & Chr(34) & " = 1"
    Dim table As Outlook.Table = _
        folder.GetTable(filter, _
        Outlook.OlTableContents.olUserItems)
    ' Remove default columns
    table.Columns.RemoveAll()
    ' Add using built-in name
    table.Columns.Add("EntryID")
    table.Columns.Add("Subject")
    table.Columns.Add("ReceivedTime")
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending)
    ' Add using namespace
    ' Date received
    table.Columns.Add( _
        "urn:schemas:httpmail:datereceived")
    While Not (table.EndOfTable)
        Dim nextRow As Outlook.Row = table.GetNextRow()
        Dim sb As StringBuilder = New StringBuilder()
        sb.AppendLine(nextRow("Subject").ToString())
        ' Reference column by name 
        sb.AppendLine("Received (Local): " _
            & nextRow("ReceivedTime").ToString())
        ' Reference column by index
        sb.AppendLine("Received (UTC): " & nextRow(4).ToString())
        sb.AppendLine()
        Debug.WriteLine(sb.ToString())
    End While
End Sub
```


```csharp
private void DemoTableColumns()
{
    const string PR_HAS_ATTACH =
        "https://schemas.microsoft.com/mapi/proptag/0x0E1B000B";
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Create filter
    string filter = "@SQL=" + "\""
        + PR_HAS_ATTACH + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    // Remove default columns
    table.Columns.RemoveAll();
    // Add using built-in name
    table.Columns.Add("EntryID");
    table.Columns.Add("Subject");
    table.Columns.Add("ReceivedTime");
    table.Sort("ReceivedTime", Outlook.OlSortOrder.olDescending);
    // Add using namespace
    // Date received
    table.Columns.Add(
        "urn:schemas:httpmail:datereceived");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine(nextRow["Subject"].ToString());
        // Reference column by name 
        sb.AppendLine("Received (Local): "
            + nextRow["ReceivedTime"]);
        // Reference column by index
        sb.AppendLine("Received (UTC): " + nextRow[4]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="acdd9-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="acdd9-113">See also</span></span>

- [<span data-ttu-id="acdd9-114">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="acdd9-114">Search and Filter</span></span>](search-and-filter.md)

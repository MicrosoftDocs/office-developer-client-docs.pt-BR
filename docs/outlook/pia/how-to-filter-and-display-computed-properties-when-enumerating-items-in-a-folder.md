---
title: Filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta
TOCTitle: Filter and display computed properties when enumerating items in a folder
ms:assetid: b068e625-ff12-444d-a30d-51a3acba3043
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184632(v=office.15)
ms:contentKeyID: 55119922
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 946858221b649cd6189ddf44680b316554cab5de
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723072"
---
# <a name="filter-and-display-computed-properties-when-enumerating-items-in-a-folder"></a><span data-ttu-id="315c3-102">Filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta</span><span class="sxs-lookup"><span data-stu-id="315c3-102">Filter and display computed properties when enumerating items in a folder</span></span>

<span data-ttu-id="315c3-103">Este exemplo mostra como filtrar e exibir propriedades calculadas ao enumerar itens em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="315c3-103">This example shows how to filter and display computed properties when enumerating items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="315c3-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="315c3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="315c3-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="315c3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="315c3-106">O objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) representa um conjunto de dados de itens de um objeto [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) ou [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="315c3-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of item data from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="315c3-107">O objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) representa linhas de dados em uma **Table** (tabela).</span><span class="sxs-lookup"><span data-stu-id="315c3-107">The [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object represents rows of data in a **Table**.</span></span> <span data-ttu-id="315c3-108">O objeto [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) representa propriedades de **Table**.</span><span class="sxs-lookup"><span data-stu-id="315c3-108">The [Columns](https://msdn.microsoft.com/library/bb646214\(v=office.15\)) object represents properties of the **Table**.</span></span> <span data-ttu-id="315c3-109">Você pode adicionar certas propriedades ao objeto **Table** usando o método [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) do objeto **Columns**.</span><span class="sxs-lookup"><span data-stu-id="315c3-109">You can add certain properties to the **Table** object by using the [Add(String)](https://msdn.microsoft.com/library/bb652865\(v=office.15\)) method of the **Columns** object.</span></span> <span data-ttu-id="315c3-110">Você pode filtrar certas propriedades usando o método [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) do objeto **Table**.</span><span class="sxs-lookup"><span data-stu-id="315c3-110">You can filter certain properties by using the [Restrict(String)](https://msdn.microsoft.com/library/bb612178\(v=office.15\)) method of the **Table** object.</span></span> <span data-ttu-id="315c3-111">No entanto, algumas propriedades não podem ser adicionadas ao objeto **Table** usando **Columns.Add**, e também não podem ser filtrados com o uso do método **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="315c3-111">However, some properties cannot be added to the **Table** object by using **Columns.Add**, nor can they be filtered by using the **Restrict** method.</span></span> <span data-ttu-id="315c3-112">A tabela a seguir descreve se propriedades têm suporte para o objeto **Table** quando se usa o método **Columns.Add** ou **Restrict**.</span><span class="sxs-lookup"><span data-stu-id="315c3-112">The following table describes whether properties are supported for the **Table** object when you use the **Columns.Add** or **Restrict** method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="315c3-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="315c3-113">Property</span></span></p></th>
<th><p><span data-ttu-id="315c3-114">Para Columns.Add</span><span class="sxs-lookup"><span data-stu-id="315c3-114">For Columns.Add</span></span></p></th>
<th><p><span data-ttu-id="315c3-115">Para Restrict</span><span class="sxs-lookup"><span data-stu-id="315c3-115">For Restrict</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="315c3-116">Propriedades binárias como <b>EntryID</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-116">Binary properties such as <b>EntryID</b>.</span></span></p></td>
<td><p><span data-ttu-id="315c3-117">Suporte por meio de propriedade interna ou de namespace.</span><span class="sxs-lookup"><span data-stu-id="315c3-117">Supported via built-in or namespace property.</span></span></p></td>
<td><p><span data-ttu-id="315c3-118">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-118">Not supported.</span></span> <span data-ttu-id="315c3-119">O Outlook irá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="315c3-119">Outlook will raise an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-120">Propriedades do corpo, incluindo <b>Body</b> e <b>HTMLBody</b>, e representação do namespace dessas propriedades, incluindo <b>PR_RTF_COMPRESSED</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-120">Body properties, including <b>Body</b> and <b>HTMLBody</b>, and namespace representation of those properties, including <b>PR_RTF_COMPRESSED</b>.</span></span></p></td>
<td><p><span data-ttu-id="315c3-121">A propriedade <b>Body</b> é suportada com a condição de que somente os primeiros 255 bytes do valor sejam armazenados em um objeto <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-121">The <b>Body</b> property is supported with a condition that only the first 255 bytes of the value are stored in a <b>Table</b> object.</span></span> <span data-ttu-id="315c3-122">Não há suporte para outras propriedades que representam o conteúdo do corpo em HTML ou RTF.</span><span class="sxs-lookup"><span data-stu-id="315c3-122">Other properties that represent the body content in HTML or RTF are not supported.</span></span> <span data-ttu-id="315c3-123">Pelo motivo de somente os primeiros 255 bytes de <b>Body</b> serem retornados, se você quiser obter o conteúdo completo do corpo de um item em texto ou HTML, use o <b>EntryID</b> do item no método <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> para obter o objeto do item.</span><span class="sxs-lookup"><span data-stu-id="315c3-123">Because only the first 255 bytes of <b>Body</b> are returned, if you want to obtain the full body content of an item in text or HTML, use the item’s <b>EntryID</b> in the <a href="https://msdn.microsoft.com/library/bb644121(v=office.15)">GetItemFromID(String, Object)</a> method to obtain the item object.</span></span> <span data-ttu-id="315c3-124">Depois, recupere o valor completo de <b>Body</b> através do objeto do item.</span><span class="sxs-lookup"><span data-stu-id="315c3-124">Then retrieve the full value of <b>Body</b> through the item object.</span></span></p></td>
<td><p><span data-ttu-id="315c3-125">Somente a propriedade <b>Body</b> representada em texto tem suporte em um filtro.</span><span class="sxs-lookup"><span data-stu-id="315c3-125">Only the <b>Body</b> property represented in text is supported in a filter.</span></span> <span data-ttu-id="315c3-126">Isso significa que a propriedade deve ser referenciada em um filtro DAV Searching and Locating (DASL) como <em>urn:schemas:http-email:textdescription</em>, e você não pode filtrar nenhuma marca HTML no corpo.</span><span class="sxs-lookup"><span data-stu-id="315c3-126">This means that the property must be referenced in a DAV Searching and Locating (DASL) filter as <em>urn:schemas:http-mail:textdescription</em>, and you cannot filter on any HTML tags in the body.</span></span> <span data-ttu-id="315c3-127">Para melhorar o desempenho, use palavras-chave do indexador de contexto no filtro para combinar cadeias de caracteres no corpo.</span><span class="sxs-lookup"><span data-stu-id="315c3-127">To improve performance, use context indexer keywords in the filter to match strings in the body.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="315c3-128">Propriedades do computador, como <b>AutoResolvedWinner</b> e <b>BodyFormat</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-128">Computer properties, such as <b>AutoResolvedWinner</b> and <b>BodyFormat</b>.</span></span></p></td>
<td><p><span data-ttu-id="315c3-129">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-129">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="315c3-130">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-130">Not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-131">Propriedades de valores múltiplos, como <b>Categories</b>, <b>Children</b>, <b>Companies</b> e <b>VotingOptions</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-131">Multivalued properties, such as <b>Categories</b>, <b>Children</b>, <b>Companies</b>, and <b>VotingOptions</b>.</span></span></p></td>
<td><p><span data-ttu-id="315c3-132">Com suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-132">Supported.</span></span></p></td>
<td><p><span data-ttu-id="315c3-133">Com suporte, desde que você possa criar uma consulta DASL usando a representação do namespace.</span><span class="sxs-lookup"><span data-stu-id="315c3-133">Supported, provided that you can create a DASL query by using the namespace representation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="315c3-134">Propriedades que retornam um objeto, como <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b> e <b>UserProperties</b>.</span><span class="sxs-lookup"><span data-stu-id="315c3-134">Properties that return an object, such as <b>Attachments</b>, <b>Parent</b>, <b>Recipients</b>, <b>RecurrencePattern</b>, and <b>UserProperties</b>.</span></span></p></td>
<td><p><span data-ttu-id="315c3-135">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-135">Not supported.</span></span></p></td>
<td><p><span data-ttu-id="315c3-136">Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="315c3-136">Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="315c3-137">A tabela a seguir lista as propriedades inválidas conhecidas que não podem ser adicionadas ao objeto **Table** com o uso de **Columns.Add**.</span><span class="sxs-lookup"><span data-stu-id="315c3-137">The following table lists known invalid properties that cannot be added to the **Table** object by using **Columns.Add**.</span></span> <span data-ttu-id="315c3-138">Se você tentar adicionar uma propriedade desta lista, o Outlook irá gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="315c3-138">If you attempt to add a property from this list, Outlook will raise an error.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="315c3-139">AutoResolvedWinner</span><span class="sxs-lookup"><span data-stu-id="315c3-139">AutoResolvedWinner</span></span></p></td>
<td><p><span data-ttu-id="315c3-140">BodyFormat</span><span class="sxs-lookup"><span data-stu-id="315c3-140">BodyFormat</span></span></p></td>
<td><p><span data-ttu-id="315c3-141">Class</span><span class="sxs-lookup"><span data-stu-id="315c3-141">Class</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-142">Companies</span><span class="sxs-lookup"><span data-stu-id="315c3-142">Companies</span></span></p></td>
<td><p><span data-ttu-id="315c3-143">ContactNames</span><span class="sxs-lookup"><span data-stu-id="315c3-143">ContactNames</span></span></p></td>
<td><p><span data-ttu-id="315c3-144">DLName</span><span class="sxs-lookup"><span data-stu-id="315c3-144">DLName</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="315c3-145">DownloadState</span><span class="sxs-lookup"><span data-stu-id="315c3-145">DownloadState</span></span></p></td>
<td><p><span data-ttu-id="315c3-146">FlagIcon</span><span class="sxs-lookup"><span data-stu-id="315c3-146">FlagIcon</span></span></p></td>
<td><p><span data-ttu-id="315c3-147">HtmlBody</span><span class="sxs-lookup"><span data-stu-id="315c3-147">HtmlBody</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-148">InternetCodePage</span><span class="sxs-lookup"><span data-stu-id="315c3-148">InternetCodePage</span></span></p></td>
<td><p><span data-ttu-id="315c3-149">IsConflict</span><span class="sxs-lookup"><span data-stu-id="315c3-149">IsConflict</span></span></p></td>
<td><p><span data-ttu-id="315c3-150">IsMarkedAsTask</span><span class="sxs-lookup"><span data-stu-id="315c3-150">IsMarkedAsTask</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="315c3-151">MeetingWorkspaceURL</span><span class="sxs-lookup"><span data-stu-id="315c3-151">MeetingWorkspaceURL</span></span></p></td>
<td><p><span data-ttu-id="315c3-152">MemberCount</span><span class="sxs-lookup"><span data-stu-id="315c3-152">MemberCount</span></span></p></td>
<td><p><span data-ttu-id="315c3-153">Permission</span><span class="sxs-lookup"><span data-stu-id="315c3-153">Permission</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-154">PermissionService</span><span class="sxs-lookup"><span data-stu-id="315c3-154">PermissionService</span></span></p></td>
<td><p><span data-ttu-id="315c3-155">RecurrenceState</span><span class="sxs-lookup"><span data-stu-id="315c3-155">RecurrenceState</span></span></p></td>
<td><p><span data-ttu-id="315c3-156">ResponseState</span><span class="sxs-lookup"><span data-stu-id="315c3-156">ResponseState</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="315c3-157">Saved</span><span class="sxs-lookup"><span data-stu-id="315c3-157">Saved</span></span></p></td>
<td><p><span data-ttu-id="315c3-158">Sent</span><span class="sxs-lookup"><span data-stu-id="315c3-158">Sent</span></span></p></td>
<td><p><span data-ttu-id="315c3-159">Submitted</span><span class="sxs-lookup"><span data-stu-id="315c3-159">Submitted</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="315c3-160">TaskSubject</span><span class="sxs-lookup"><span data-stu-id="315c3-160">TaskSubject</span></span></p></td>
<td><p><span data-ttu-id="315c3-161">Unread</span><span class="sxs-lookup"><span data-stu-id="315c3-161">Unread</span></span></p></td>
<td><p><span data-ttu-id="315c3-162">VotingOptions</span><span class="sxs-lookup"><span data-stu-id="315c3-162">VotingOptions</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="315c3-163">Embora algumas propriedades calculadas não possam ser adicionadas à coluna definida para uma tabela, o seguinte exemplo de código funciona para contornar esta limitação.</span><span class="sxs-lookup"><span data-stu-id="315c3-163">Although some computed properties cannot be added to the column set for a table, the following code example works around this limitation.</span></span> <span data-ttu-id="315c3-164">GetToDoItems usa uma consulta DASL para restringir os itens que aparecem em **Table**.</span><span class="sxs-lookup"><span data-stu-id="315c3-164">GetToDoItems uses a DASL query to restrict the items that appear in the **Table**.</span></span> <span data-ttu-id="315c3-165">Se a propriedade computada tem uma representação de namespace, a representação de namespace é usada para criar uma consulta DASL que restringe o objeto **Table** para retornar linhas de um valor específico da propriedade calculada.</span><span class="sxs-lookup"><span data-stu-id="315c3-165">If the computed property has a namespace representation, the namespace representation is used to create a DASL query that restricts the **Table** object to return rows for a specified value of the computed property.</span></span> <span data-ttu-id="315c3-166">GetToDoItems coloca itens na Caixa de Entrada onde o valor da propriedade [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) é igual a **verdadeiro**, e depois atribui valores a determinadas propriedades de tarefas como [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)) e [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="315c3-166">GetToDoItems gets items in the Inbox where the value of the [IsMarkedAsTask](https://msdn.microsoft.com/library/bb623631\(v=office.15\)) property is equal to **true**, and then assigns values to certain task properties such as [TaskSubject](https://msdn.microsoft.com/library/bb643880\(v=office.15\)), [TaskDueDate](https://msdn.microsoft.com/library/bb623035\(v=office.15\)), [TaskStartDate](https://msdn.microsoft.com/library/bb610832\(v=office.15\)), and [TaskCompletedDate](https://msdn.microsoft.com/library/bb624055\(v=office.15\)).</span></span> <span data-ttu-id="315c3-167">Finalmente, essas propriedades são escritas para rastrear ouvintes da coleção [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="315c3-167">Finally, those properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="315c3-168">Se usar o Visual Studio para testar este exemplo de código, adicione primeiro uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especifique a variável do Outlook quando importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="315c3-168">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="315c3-169">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="315c3-169">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="315c3-170">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="315c3-170">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetToDoItems()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // DASL filter for IsMarkedAsTask
    string filter = "@SQL=" + "\"" +
        "https://schemas.microsoft.com/mapi/proptag/0x0E2B0003"
        + "\"" + " = 1";
    Outlook.Table table =
        folder.GetTable(filter,
        Outlook.OlTableContents.olUserItems);
    table.Columns.Add("TaskStartDate");
    table.Columns.Add("TaskDueDate");
    table.Columns.Add("TaskCompletedDate");
    // Use GUID/ID to represent TaskSubject
    table.Columns.Add(
        "https://schemas.microsoft.com/mapi/id/" +
        "{00062008-0000-0000-C000-000000000046}/85A4001E");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Task Subject: " + nextRow[9]);
        sb.AppendLine("Start Date: "
            + nextRow["TaskStartDate"]);
        sb.AppendLine("Due Date: "
            + nextRow["TaskDueDate"]);
        sb.AppendLine("Completed Date: "
            + nextRow["TaskCompletedDate"]);
        sb.AppendLine();
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="315c3-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="315c3-171">See also</span></span>

- [<span data-ttu-id="315c3-172">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="315c3-172">Search and filter</span></span>](search-and-filter.md)


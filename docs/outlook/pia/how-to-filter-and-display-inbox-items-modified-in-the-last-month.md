---
title: Filtro e exibir os itens de caixa de entrada modificados no mês passado
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 952d28cc64ffa3638f8147b665e88a372dc81848
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406873"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a><span data-ttu-id="46117-102">Filtro e exibir os itens de caixa de entrada modificados no mês passado</span><span class="sxs-lookup"><span data-stu-id="46117-102">Filter and display Inbox items modified in the last month</span></span>

<span data-ttu-id="46117-103">Este exemplo mostra como filtrar e exibir os itens de caixa de entrada que foram modificados no mês passado.</span><span class="sxs-lookup"><span data-stu-id="46117-103">This example shows how to filter and display Inbox items that were modified in the last month.</span></span>

## <a name="example"></a><span data-ttu-id="46117-104">Exemplo</span><span class="sxs-lookup"><span data-stu-id="46117-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="46117-105">O exemplo de código a seguir é um trecho de [Programar aplicativos para o Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="46117-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="46117-106">A linguagem de consulta DAV Searching and Locating (DASL) se baseia na implementação do Microsoft Exchange do DASL no Outlook.</span><span class="sxs-lookup"><span data-stu-id="46117-106">DAV Searching and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook.</span></span> <span data-ttu-id="46117-107">Pode ser usada para retornar resultados com base em propriedades para pesquisas em nível de item nos dados de pastas, como os representados por um objeto [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="46117-107">It can be used to return property-based results for item-level searches in folder data, such as that represented by a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="46117-108">Os filtros DASL suportam comparações de cadeias de caracteres, incluindo equivalência, prefixo, frase e correspondência de subcadeias, usando o operado igual (=).</span><span class="sxs-lookup"><span data-stu-id="46117-108">DASL filters support string comparisons, including equivalence, prefix, phrase, and substring matching, by using the equal (=) operator.</span></span> <span data-ttu-id="46117-109">É possível usar consultas DASL para executar comparações e filtragens de data-hora.</span><span class="sxs-lookup"><span data-stu-id="46117-109">You can use DASL queries to perform date-time comparison and filtering.</span></span>

<span data-ttu-id="46117-110">Como as consultas DASL sempre executam comparações **DateTime** em Tempo Universal Coordenado (UTC), é necessário converter o valor da hora local para UTC para que a consulta funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="46117-110">Because DASL queries always perform **DateTime** comparisons in Coordinated Universal Time (UTC), you must convert the local time value to UTC if you want the query to operate correctly.</span></span> <span data-ttu-id="46117-111">Você também deve converter o valor de **DateTime** em uma representação de cadeia de caracteres, pois os filtros DASL suportam comparações de cadeias.</span><span class="sxs-lookup"><span data-stu-id="46117-111">You must also convert the **DateTime** value to a string representation because DASL filters support string comparisons.</span></span> <span data-ttu-id="46117-112">Você pode fazer a conversão **Date Time** de duas maneiras: usando o método [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) do objeto [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)), ou usando as macros **DateTime**do Outlook para fazer a conversão.</span><span class="sxs-lookup"><span data-stu-id="46117-112">You can make the **DateTime** conversion in two ways: by using the [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) method of the [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object, or by using Outlook **DateTime** macros to make the conversion.</span></span>

<span data-ttu-id="46117-113">A seguinte linha de código mostra como usar o método**LocalTimeToUTC** para converter o valor da propriedade **LastModificationTime** (que é uma coluna padrão em todos os objetos **Item**) para UTC.</span><span class="sxs-lookup"><span data-stu-id="46117-113">The following line of code shows how to use the **LocalTimeToUTC** method to convert the value of the **LastModificationTime** property (which is a default column in all **Item** objects) to UTC.</span></span>

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

<span data-ttu-id="46117-114">A tabela seguinte lista as macros **DateTime** que você pode usar para retornar cadeias de caracteres filtradas que comparam o valor de uma propriedade **DateTime** determinada com uma data relativa especificada ou com um intervalo de datas em UTC.</span><span class="sxs-lookup"><span data-stu-id="46117-114">The following table lists the **DateTime** macros you can use to return filtered strings that compare the value of a given **DateTime** property with a specified relative date or date range in UTC.</span></span> <span data-ttu-id="46117-115">O valor de propriedade SchemaName representa um qualquer propriedade **DateTime** válida referenciada por namespace.</span><span class="sxs-lookup"><span data-stu-id="46117-115">The SchemaName property value represents any valid **DateTime** property referenced by namespace.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46117-116">Macro</span><span class="sxs-lookup"><span data-stu-id="46117-116">Macro</span></span></p></th>
<th><p><span data-ttu-id="46117-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46117-117">Syntax</span></span></p></th>
<th><p><span data-ttu-id="46117-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="46117-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46117-119">today</span><span class="sxs-lookup"><span data-stu-id="46117-119">today</span></span></p></td>
<td><p><span data-ttu-id="46117-120">%today(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-120">%today(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-121">Restringe aos itens com valor de propriedade SchemaName igual a hoje.</span><span class="sxs-lookup"><span data-stu-id="46117-121">Restricts for items with SchemaName property value equal to today</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46117-122">tomorrow</span><span class="sxs-lookup"><span data-stu-id="46117-122">tomorrow</span></span></p></td>
<td><p><span data-ttu-id="46117-123">%tomorrow(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-123">%tomorrow(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-124">Restringe aos itens com valor de propriedade SchemaName igual a amanhã.</span><span class="sxs-lookup"><span data-stu-id="46117-124">Restricts for items with SchemaName property value equal to tomorrow</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46117-125">yesterday</span><span class="sxs-lookup"><span data-stu-id="46117-125">yesterday</span></span></p></td>
<td><p><span data-ttu-id="46117-126">%yesterday(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-126">%yesterday(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-127">Restringe aos itens com valor de propriedade SchemaName igual a ontem.</span><span class="sxs-lookup"><span data-stu-id="46117-127">Restricts for items with SchemaName property value equal to yesterday</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46117-128">next7days</span><span class="sxs-lookup"><span data-stu-id="46117-128">next7days</span></span></p></td>
<td><p><span data-ttu-id="46117-129">%next7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-129">%next7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-130">Restringir aos itens com valores de propriedade SchemaName em um intervalo equivalente aos próximos sete dias.</span><span class="sxs-lookup"><span data-stu-id="46117-130">Restricts for items with SchemaName property values in a range equivalent to the next seven days.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46117-131">last7days</span><span class="sxs-lookup"><span data-stu-id="46117-131">last7days</span></span></p></td>
<td><p><span data-ttu-id="46117-132">%last7days(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-132">%last7days(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-133">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente aos últimos sete dias.</span><span class="sxs-lookup"><span data-stu-id="46117-133">Restricts for items with SchemaName property values in a range equivalent to the last seven days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46117-134">nextweek</span><span class="sxs-lookup"><span data-stu-id="46117-134">nextweek</span></span></p></td>
<td><p><span data-ttu-id="46117-135">%nextweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-135">%nextweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-136">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente à próxima semana.</span><span class="sxs-lookup"><span data-stu-id="46117-136">Restricts for items with SchemaName property values in a range equivalent to next week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46117-137">thisweek</span><span class="sxs-lookup"><span data-stu-id="46117-137">thisweek</span></span></p></td>
<td><p><span data-ttu-id="46117-138">%thisweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-138">%thisweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-139">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente a esta semana.</span><span class="sxs-lookup"><span data-stu-id="46117-139">Restricts for items with SchemaName property values in a range equivalent to this week.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46117-140">lastweek</span><span class="sxs-lookup"><span data-stu-id="46117-140">lastweek</span></span></p></td>
<td><p><span data-ttu-id="46117-141">%lastweek(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-141">%lastweek(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-142">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente à última semana.</span><span class="sxs-lookup"><span data-stu-id="46117-142">Restricts for items with SchemaName property values in a range equivalent to last week.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46117-143">nextmonth</span><span class="sxs-lookup"><span data-stu-id="46117-143">nextmonth</span></span></p></td>
<td><p><span data-ttu-id="46117-144">%nextmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-144">%nextmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-145">Restringe aos itens com valores de propriedade em um intervalo equivalente ao próximo mês.</span><span class="sxs-lookup"><span data-stu-id="46117-145">Restricts for items with SchemaName property values in a range equivalent to next month.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46117-146">thismonth</span><span class="sxs-lookup"><span data-stu-id="46117-146">thismonth</span></span></p></td>
<td><p><span data-ttu-id="46117-147">%thismonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-147">%thismonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-148">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente a este mês.</span><span class="sxs-lookup"><span data-stu-id="46117-148">Restricts for items with SchemaName property values in a range equivalent to this month.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46117-149">lastmonth</span><span class="sxs-lookup"><span data-stu-id="46117-149">lastmonth</span></span></p></td>
<td><p><span data-ttu-id="46117-150">%lastmonth(“SchemaName”)%</span><span class="sxs-lookup"><span data-stu-id="46117-150">%lastmonth(“SchemaName”)%</span></span></p></td>
<td><p><span data-ttu-id="46117-151">Restringe aos itens com valores de propriedade SchemaName em um intervalo equivalente ao último mês.</span><span class="sxs-lookup"><span data-stu-id="46117-151">Restricts for items with SchemaName property values in a range equivalent to last month.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46117-152">No exemplo a seguir DemoDASLDateMacro cria uma consulta DASL que usa a macro **lastmonthDateTime** para filtrar os itens na caixa de entrada do usuário que foram modificados no mês passado.</span><span class="sxs-lookup"><span data-stu-id="46117-152">In the following example, DemoDASLDateMacro creates a DASL query that uses the **lastmonthDateTime** macro to filter for items in the user’s Inbox that were modified in the last month.</span></span> <span data-ttu-id="46117-153">Em seguida, cria um objeto **Table** com esse filtro, e enumera e exibe as linhas no objeto **Table** restrito.</span><span class="sxs-lookup"><span data-stu-id="46117-153">It then creates a **Table** object with that filter, and enumerates and displays the rows in the restricted **Table** object.</span></span>

<span data-ttu-id="46117-154">Se usar o Visual Studio para testar este exemplo de código, você precisa primeiro adicionar uma referência ao componente da biblioteca de objetos do Microsoft Outlook 15.0 e especificar a variável do Outlook quando você importar o namespace **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="46117-154">
    If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the \*\*Microsoft.Office.Interop.Outlook\*\* namespace. The using statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C#.
</span></span> <span data-ttu-id="46117-155">O \*\* que usa a instrução\*\* não deve ocorrer diretamente antes das funções no exemplo de código, mas precisa ser adicionado antes da declaração de Classe pública.</span><span class="sxs-lookup"><span data-stu-id="46117-155">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="46117-156">A linha de código seguinte mostra como fazer a importação e atribuição em C\#.</span><span class="sxs-lookup"><span data-stu-id="46117-156">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="46117-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="46117-157">See also</span></span>

- [<span data-ttu-id="46117-158">Pesquisar e filtrar</span><span class="sxs-lookup"><span data-stu-id="46117-158">Search and Filter</span></span>](search-and-filter.md)


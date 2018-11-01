---
title: Operação UNION (SQL do Microsoft Access)
TOCTitle: UNION Operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 63ff883f35dabbbd69e1bf144eb32016f303c7ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879106"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="69f47-102">Operação UNION (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="69f47-102">UNION Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="69f47-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="69f47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69f47-104">Cria uma consulta união, que combina os resultados de duas ou mais consultas ou tabelas independentes.</span><span class="sxs-lookup"><span data-stu-id="69f47-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69f47-105">Syntax</span></span>

<span data-ttu-id="69f47-106">\[TABELA\] *Consulta1* união \[todas as\] \[tabela\] *consulta2* \[união \[todas as\] \[tabela\] *queryn* \[ …</span><span class="sxs-lookup"><span data-stu-id="69f47-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="69f47-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="69f47-107"></span></span>

<span data-ttu-id="69f47-108">A operação UNION contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="69f47-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="69f47-109">Parte</span><span class="sxs-lookup"><span data-stu-id="69f47-109">Part</span></span></p></th>
<th><p><span data-ttu-id="69f47-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="69f47-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69f47-111"><em>query1-n</em></span><span class="sxs-lookup"><span data-stu-id="69f47-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="69f47-112">Uma instrução SELECT, o nome de uma consulta armazenada ou o nome de uma tabela armazenada precedida pela palavra-chave TABLE.</span><span class="sxs-lookup"><span data-stu-id="69f47-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="69f47-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="69f47-113">Remarks</span></span>

<span data-ttu-id="69f47-p102">Você pode mesclar os resultados de duas ou mais consultas, tabelas e instruções SELECT, em qualquer combinação, em uma única operação UNION. O exemplo a seguir mescla uma tabela existente chamada Novas Contas e uma instrução SELECT:</span><span class="sxs-lookup"><span data-stu-id="69f47-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="69f47-p103">Por padrão, nenhum registro duplicado é retornado quando você usa uma operação UNION; contudo, você pode incluir o predicado [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) para garantir que todos os registros sejam retornados. Isso também faz com que a consulta seja executada de modo mais rápido.</span><span class="sxs-lookup"><span data-stu-id="69f47-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="69f47-118">Todas as consultas em uma operação UNION devem solicitar o mesmo número de campos; entretanto, os campos não têm que ser do mesmo tamanho nem do mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="69f47-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="69f47-p104">Use aliases somente na primeira instrução SELECT, porque eles são ignorados em quaisquer outras instruções. Na cláusula ORDER BY, refira-se aos campos pelo modo como são chamados na primeira instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="69f47-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="69f47-121">Você pode usar uma cláusula <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> ou <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> em cada argumento <EM>query</EM> para agrupar os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="69f47-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="69f47-122">Você pode usar uma cláusula <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> no final do último argumento <EM>query</EM> para exibir os dados retornados em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="69f47-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="69f47-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="69f47-123">Example</span></span>

<span data-ttu-id="69f47-124">Este exemplo recupera os nomes e as cidades de todos os fornecedores e clientes no Brasil.</span><span class="sxs-lookup"><span data-stu-id="69f47-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span>

<span data-ttu-id="69f47-125">Este exemplo chama o procedimento EnumFields, que pode ser localizado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="69f47-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```

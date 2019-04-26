---
title: Operação UNION (SQL do Microsoft Access)
TOCTitle: UNION operation (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314697"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="80cfd-102">Operação UNION (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="80cfd-102">UNION Operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="80cfd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="80cfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="80cfd-104">Cria uma consulta união, que combina os resultados de duas ou mais consultas ou tabelas independentes.</span><span class="sxs-lookup"><span data-stu-id="80cfd-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="80cfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80cfd-105">Syntax</span></span>

<span data-ttu-id="80cfd-106">\[TABLE\] *consulta1* UNION \[ALL\] \[TABLE\] *consulta2* \[UNION \[ALL\] \[TABLE\] *consultan* \[ …</span><span class="sxs-lookup"><span data-stu-id="80cfd-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="80cfd-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="80cfd-107"></span></span>

<span data-ttu-id="80cfd-108">A operação UNION tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="80cfd-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="80cfd-109">Sair</span><span class="sxs-lookup"><span data-stu-id="80cfd-109">Part</span></span></p></th>
<th><p><span data-ttu-id="80cfd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="80cfd-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80cfd-111"><em>consulta1-n</em></span><span class="sxs-lookup"><span data-stu-id="80cfd-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="80cfd-112">Uma instrução SELECT, o nome de uma consulta armazenada ou o nome de uma tabela armazenada precedida pela palavra-chave TABLE.</span><span class="sxs-lookup"><span data-stu-id="80cfd-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="80cfd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="80cfd-113">Remarks</span></span>

<span data-ttu-id="80cfd-p102">É possível mesclar os resultados de duas ou mais consultas, tabelas e instruções SELECT, em qualquer combinação, em uma única operação UNION. O exemplo a seguir mescla uma tabela existente chamada New Accounts e uma instrução SELECT:</span><span class="sxs-lookup"><span data-stu-id="80cfd-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="80cfd-p103">Por padrão, nenhum registro duplicado é retornado quando você usa uma operação UNION; contudo, você pode incluir o predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para garantir que todos os registros sejam retornados. Isso também faz com que a consulta seja executada de modo mais rápido.</span><span class="sxs-lookup"><span data-stu-id="80cfd-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="80cfd-118">Todas as consultas em uma operação UNION devem solicitar o mesmo número de campos; entretanto, os campos não têm que ser do mesmo tamanho nem do mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="80cfd-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="80cfd-p104">Use aliases apenas na primeira instrução SELECT, porque eles são ignorados em quaisquer outras. Na cláusula ORDER BY, faça referência aos campos pelos quais eles são chamados na primeira instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="80cfd-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="80cfd-121">Você pode usar uma cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) em cada argumento *query* para agrupar os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="80cfd-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="80cfd-122">Você pode usar uma cláusula [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) no final do último argumento *query* para exibir dados retornados em um ordem específica.</span><span class="sxs-lookup"><span data-stu-id="80cfd-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="80cfd-123">Exemplo</span><span class="sxs-lookup"><span data-stu-id="80cfd-123">Example</span></span>

<span data-ttu-id="80cfd-124">Este exemplo recupera os nomes e cidades de todos os clientes e fornecedores no Brasil.</span><span class="sxs-lookup"><span data-stu-id="80cfd-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="80cfd-125">Ele é chamado procedimento EnumFields, e pode ser encontrado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="80cfd-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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

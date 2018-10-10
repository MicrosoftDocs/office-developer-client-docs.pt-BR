---
title: Subconsultas SQL (SQL do Microsoft Access)
TOCTitle: SQL Subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 091dc4aa26d653c6e556fc7540e4b65f29d501ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465223"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="fd02d-102">Subconsultas SQL (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="fd02d-102">SQL Subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="fd02d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd02d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd02d-104">Uma subconsulta é uma instrução [SELECT](select-statement-microsoft-access-sql.md) aninhada dentro de uma instrução SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md) ou dentro de outra subconsulta.</span><span class="sxs-lookup"><span data-stu-id="fd02d-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd02d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd02d-105">Syntax</span></span>

<span data-ttu-id="fd02d-106">Você pode usar três formas de sintaxe para criar uma subconsulta:</span><span class="sxs-lookup"><span data-stu-id="fd02d-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="fd02d-107">*comparação* \[ANY | TODOS OS | Alguns\] (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="fd02d-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span></span>

<span data-ttu-id="fd02d-108">*expressão* \[Não\] em (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="fd02d-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="fd02d-109">\[NÃO\] EXISTS (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="fd02d-109">\[NOT\] EXISTS (*sqlstatement*)</span></span>

<span data-ttu-id="fd02d-110">Uma subconsulta contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="fd02d-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd02d-111">Parte</span><span class="sxs-lookup"><span data-stu-id="fd02d-111">Part</span></span></p></th>
<th><p><span data-ttu-id="fd02d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd02d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd02d-113"><em>comparison</em></span><span class="sxs-lookup"><span data-stu-id="fd02d-113"><em>comparison</em></span></span></p></td>
<td><p><span data-ttu-id="fd02d-114">Uma expressão e uma operador de comparação que compara a expressão com os resultados da subconsulta.</span><span class="sxs-lookup"><span data-stu-id="fd02d-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd02d-115"><em>expressão</em></span><span class="sxs-lookup"><span data-stu-id="fd02d-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="fd02d-116">Uma expressão na qual o resultado definido da subconsulta é pesquisado.</span><span class="sxs-lookup"><span data-stu-id="fd02d-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd02d-117"><em>sqlstatement</em></span><span class="sxs-lookup"><span data-stu-id="fd02d-117"><em>sqlstatement</em></span></span></p></td>
<td><p><span data-ttu-id="fd02d-p101">Uma instrução SELECT, seguindo o mesmo formato e as mesmas regras que qualquer outra instrução SELECT. Ela deve estar entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="fd02d-p101">A SELECT statement, following the same format and rules as any other SELECT statement. It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fd02d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd02d-120">Remarks</span></span>

<span data-ttu-id="fd02d-p102">Você pode usar uma subconsulta em vez de uma expressão na lista de campos de uma instrução SELECT ou em uma cláusula [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) ou [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)). Em uma subconsulta, use uma instrução SELECT para fornecer um conjunto de um ou mais valores específicos para serem avaliados na expressão da cláusula WHERE ou HAVING.</span><span class="sxs-lookup"><span data-stu-id="fd02d-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) or [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="fd02d-p103">Use o predicado ANY ou SOME, que são sinônimos, para recuperar registros na consulta principal que atenda à comparação com qualquer registro recuperado na subconsulta. O exemplo a seguir retorna todos os produtos cujo preço de unidade é maior que o preço de qualquer outro produto vendido com um desconto de 25% ou mais:</span><span class="sxs-lookup"><span data-stu-id="fd02d-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="fd02d-p104">Use o predicado [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) para recuperar somente aqueles registros na consulta principal que atendam à comparação com todos os registros recuperados na subconsulta. Se você mudar de ANY para ALL no exemplo anterior, a consulta retornará somente aqueles produtos cujo preço da unidade for maior que o preço de todos os produtos vendidos com um desconto de 25% ou mais. Isso é muito mais restritivo.</span><span class="sxs-lookup"><span data-stu-id="fd02d-p104">Use the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="fd02d-p105">Use o predicado IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual. O exemplo a seguir retorna todos os produtos com um desconto de 25% ou mais:</span><span class="sxs-lookup"><span data-stu-id="fd02d-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="fd02d-130">De modo oposto, você NÃO pode usar IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual.</span><span class="sxs-lookup"><span data-stu-id="fd02d-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="fd02d-131">Use o predicado EXISTS (com a palavra reservada opcional NOT) em comparações true/false para determinar se a subconsulta retorna algum registro.</span><span class="sxs-lookup"><span data-stu-id="fd02d-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="fd02d-p106">Você também pode usar os aliases do nome da tabela em um subconsulta para se referir a tabelas listadas em uma cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) fora da subconsulta. O exemplo a seguir retorna os nomes de funcionários cujos salários são iguais ou maiores que o salário médio de todos os funcionários que têm o mesmo cargo. A tabela Funcionários recebe o alias "T1":</span><span class="sxs-lookup"><span data-stu-id="fd02d-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="fd02d-135">No exemplo anterior, a palavra reservada AS é opcional.</span><span class="sxs-lookup"><span data-stu-id="fd02d-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="fd02d-p107">Algumas subconsultas são permitidas em consultas de de tabela de referência cruzada  especificamente, como predicados (aqueles na cláusula WHERE). As subconsultas como saída (aquelas na lista SELECT) não são permitidas nas consultas de tabela de referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="fd02d-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="fd02d-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fd02d-138">Example</span></span>

<span data-ttu-id="fd02d-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span><span class="sxs-lookup"><span data-stu-id="fd02d-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span>

<span data-ttu-id="fd02d-140">Este exemplo chama o procedimento EnumFields, que pode ser localizado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="fd02d-140">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```

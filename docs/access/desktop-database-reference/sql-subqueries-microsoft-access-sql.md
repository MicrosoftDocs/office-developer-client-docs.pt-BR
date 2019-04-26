---
title: Subconsultas SQL (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
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
localization_priority: Priority
ms.openlocfilehash: 7beda04d1f18014101f00078de1d125c1fd67a69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314564"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="d036e-102">Subconsultas SQL (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="d036e-102">SQL Subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="d036e-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d036e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d036e-104">Uma subconsulta é uma instrução [SELECT](select-statement-microsoft-access-sql.md) aninhada dentro de uma instrução SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md) ou dentro de outra subconsulta.</span><span class="sxs-lookup"><span data-stu-id="d036e-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="d036e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d036e-105">Syntax</span></span>

<span data-ttu-id="d036e-106">Você pode usar três formas de sintaxe para criar uma subconsulta:</span><span class="sxs-lookup"><span data-stu-id="d036e-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="d036e-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="d036e-107">comparison [ANY | ALL | SOME] (sqlstatement)</span></span>

<span data-ttu-id="d036e-108">*expression* \[NOT\] IN (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="d036e-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="d036e-109">\[NOT\] EXISTS (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="d036e-109">[NOT] EXISTS (sqlstatement)</span></span>

<span data-ttu-id="d036e-110">Uma subconsulta contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="d036e-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d036e-111">Sair</span><span class="sxs-lookup"><span data-stu-id="d036e-111">Part</span></span></p></th>
<th><p><span data-ttu-id="d036e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d036e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d036e-113"><em>comparação</em></span><span class="sxs-lookup"><span data-stu-id="d036e-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="d036e-114">Uma expressão e uma operador de comparação que compara a expressão com os resultados da subconsulta.</span><span class="sxs-lookup"><span data-stu-id="d036e-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d036e-115"><em>expressão</em></span><span class="sxs-lookup"><span data-stu-id="d036e-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="d036e-116">Uma expressão na qual o resultado definido da subconsulta é pesquisado.</span><span class="sxs-lookup"><span data-stu-id="d036e-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d036e-117"><em>sqlstatement</em></span><span class="sxs-lookup"><span data-stu-id="d036e-117"><em>SQLStatement</em></span></span></p></td>
<td><p><span data-ttu-id="d036e-118">Uma instrução SELECT, seguindo o mesmo formato e as mesmas regras que qualquer outra instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="d036e-118">A SELECT statement, following the same format and rules as any other SELECT statement.</span></span> <span data-ttu-id="d036e-119">Ela deve estar entre parênteses.</span><span class="sxs-lookup"><span data-stu-id="d036e-119">It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d036e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d036e-120">Remarks</span></span>

<span data-ttu-id="d036e-p102">Você pode usar uma subconsulta em vez de uma expressão na lista de campos de uma instrução SELECT ou em uma cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). Em uma subconsulta, use uma instrução SELECT para fornecer um conjunto de um ou mais valores específicos para serem avaliados na expressão da cláusula WHERE ou HAVING.</span><span class="sxs-lookup"><span data-stu-id="d036e-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="d036e-p103">Use o predicado ANY ou SOME, que são sinônimos, para recuperar registros na consulta principal que atenda à comparação com qualquer registro recuperado na subconsulta. O exemplo a seguir retorna todos os produtos cujo preço de unidade é maior que o preço de qualquer outro produto vendido com um desconto de 25% ou mais:</span><span class="sxs-lookup"><span data-stu-id="d036e-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="d036e-p104">Use o predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para recuperar somente aqueles registros na consulta principal que atendam à comparação com todos os registros recuperados na subconsulta. Se você mudar de ANY para ALL no exemplo anterior, a consulta retornará somente aqueles produtos cujo preço da unidade for maior que o preço de todos os produtos vendidos com um desconto de 25% ou mais. Isso é muito mais restritivo.</span><span class="sxs-lookup"><span data-stu-id="d036e-p104">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="d036e-p105">Use o predicado IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual. O exemplo a seguir retorna todos os produtos com um desconto de 25% ou mais:</span><span class="sxs-lookup"><span data-stu-id="d036e-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="d036e-130">De modo oposto, você NÃO pode usar IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual.</span><span class="sxs-lookup"><span data-stu-id="d036e-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="d036e-131">Use o predicado EXISTS (com a palavra reservada opcional NOT) em comparações true/false para determinar se a subconsulta retorna algum registro.</span><span class="sxs-lookup"><span data-stu-id="d036e-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="d036e-p106">Você também pode usar os aliases do nome da tabela em um subconsulta para se referir a tabelas listadas em uma cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) fora da subconsulta. O exemplo a seguir retorna os nomes de funcionários cujos salários são iguais ou maiores que o salário médio de todos os funcionários que têm o mesmo cargo. A tabela Funcionários recebe o alias "T1":</span><span class="sxs-lookup"><span data-stu-id="d036e-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="d036e-135">No exemplo anterior, a palavra reservada AS é opcional.</span><span class="sxs-lookup"><span data-stu-id="d036e-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="d036e-p107">Algumas subconsultas são permitidas em consultas de de tabela de referência cruzada  especificamente, como predicados (aqueles na cláusula WHERE). As subconsultas como saída (aquelas na lista SELECT) não são permitidas nas consultas de tabela de referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="d036e-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="d036e-138">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d036e-138">Example</span></span>

<span data-ttu-id="d036e-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span><span class="sxs-lookup"><span data-stu-id="d036e-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="d036e-140">Ele chama o procedimento EnumFields, o qual você pode encontrar no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="d036e-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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

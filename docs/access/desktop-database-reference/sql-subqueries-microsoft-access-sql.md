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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722869"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>Subconsultas SQL (Microsoft Access SQL)


**Aplica-se a**: Access 2013, o Office 2013

Uma subconsulta é uma instrução [SELECT](select-statement-microsoft-access-sql.md) aninhada dentro de uma instrução SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md) ou [UPDATE](update-statement-microsoft-access-sql.md) ou dentro de outra subconsulta.

## <a name="syntax"></a>Sintaxe

Você pode usar três formas de sintaxe para criar uma subconsulta:

*comparação* \[ANY | TODOS OS | Alguns\] (*sqlstatement*)

*expressão* \[Não\] em (*sqlstatement*)

\[NÃO\] EXISTS (*sqlstatement*)

Uma subconsulta contém estas partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>comparison</em></p></td>
<td><p>Uma expressão e uma operador de comparação que compara a expressão com os resultados da subconsulta.</p></td>
</tr>
<tr class="even">
<td><p><em>expressão</em></p></td>
<td><p>Uma expressão na qual o resultado definido da subconsulta é pesquisado.</p></td>
</tr>
<tr class="odd">
<td><p><em>sqlstatement</em></p></td>
<td><p>Uma instrução SELECT, seguindo o mesmo formato e as mesmas regras que qualquer outra instrução SELECT. Ela deve estar entre parênteses.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar uma subconsulta em vez de uma expressão na lista de campos de uma instrução SELECT ou em uma cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql). Em uma subconsulta, use uma instrução SELECT para fornecer um conjunto de um ou mais valores específicos para serem avaliados na expressão da cláusula WHERE ou HAVING.

Use o predicado ANY ou SOME, que são sinônimos, para recuperar registros na consulta principal que atenda à comparação com qualquer registro recuperado na subconsulta. O exemplo a seguir retorna todos os produtos cujo preço de unidade é maior que o preço de qualquer outro produto vendido com um desconto de 25% ou mais:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Use o predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para recuperar somente aqueles registros na consulta principal que atendam à comparação com todos os registros recuperados na subconsulta. Se você mudar de ANY para ALL no exemplo anterior, a consulta retornará somente aqueles produtos cujo preço da unidade for maior que o preço de todos os produtos vendidos com um desconto de 25% ou mais. Isso é muito mais restritivo.

Use o predicado IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual. O exemplo a seguir retorna todos os produtos com um desconto de 25% ou mais:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

De modo oposto, você NÃO pode usar IN para recuperar somente aqueles registros na consulta principal para os quais algum registro na subconsulta contém um valor igual.

Use o predicado EXISTS (com a palavra reservada opcional NOT) em comparações true/false para determinar se a subconsulta retorna algum registro.

Você também pode usar os aliases do nome da tabela em um subconsulta para se referir a tabelas listadas em uma cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) fora da subconsulta. O exemplo a seguir retorna os nomes de funcionários cujos salários são iguais ou maiores que o salário médio de todos os funcionários que têm o mesmo cargo. A tabela Funcionários recebe o alias "T1":

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

No exemplo anterior, a palavra reservada AS é opcional.

Algumas subconsultas são permitidas em consultas de de tabela de referência cruzada  especificamente, como predicados (aqueles na cláusula WHERE). As subconsultas como saída (aquelas na lista SELECT) não são permitidas nas consultas de tabela de referência cruzada.

## <a name="example"></a>Exemplo

This example lists the name and contact of every customer who placed an order in the second quarter of 1995. Ele chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.

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

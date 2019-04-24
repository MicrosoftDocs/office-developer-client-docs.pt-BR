---
title: Operações LEFT JOIN RIGHT JOIN (SQL do Microsoft Access)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290142"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="a716d-102">Operações LEFT JOIN RIGHT JOIN (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="a716d-102">LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="a716d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a716d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a716d-104">Combina registros da tabela de origem quando usados em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="a716d-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="a716d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a716d-105">Syntax</span></span>

<span data-ttu-id="a716d-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span><span class="sxs-lookup"><span data-stu-id="a716d-106">FROM *table1* \[ [ LEFT | RIGHT ] JOIN *table2* 
    ON \*table1.field1 \* *compopr table2.field2*</span></span>

<span data-ttu-id="a716d-107">As operações LEFT JOIN e RIGHT JOIN têm estas partes:</span><span class="sxs-lookup"><span data-stu-id="a716d-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a716d-108">Parte</span><span class="sxs-lookup"><span data-stu-id="a716d-108">Part</span></span></p></th>
<th><p><span data-ttu-id="a716d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a716d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a716d-110"><em>tabela1</em>, <em>tabela2</em></span><span class="sxs-lookup"><span data-stu-id="a716d-110"><em>table1</em>  ,  <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="a716d-111">Os nomes das tabelas das quais os registros são combinados.</span><span class="sxs-lookup"><span data-stu-id="a716d-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a716d-112"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="a716d-112"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="a716d-p101">Os nomes dos campos unidos. Os campos devem ser do mesmo tipo de dados e conter o mesmo tipo de dados, mas não precisam ter o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="a716d-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a716d-115"><em>oprcomp</em></span><span class="sxs-lookup"><span data-stu-id="a716d-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="a716d-116">Qualquer operador de comparação relacional: &quot;=&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=&quot; &quot; &gt; =&quot; ou &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="a716d-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a716d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a716d-117">Remarks</span></span>

<span data-ttu-id="a716d-p102">Use a operação LEFT JOIN para criar uma junção externa esquerda. As junções externas esquerdas incluem todos os registros da primeira de duas tabelas (a da esquerda), mesmo se não houver valores correspondentes na segunda tabela (à direita).</span><span class="sxs-lookup"><span data-stu-id="a716d-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="a716d-p103">Use uma operação RIGHT JOIN para criar uma junção externa direita. As junções externas direitas incluem todos os registros da segunda de duas tabelas (a da direita), mesmo se não houver valores correspondentes para registros na primeira tabela (à esquerda).</span><span class="sxs-lookup"><span data-stu-id="a716d-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="a716d-p104">Por exemplo, você poderia usar LEFT JOIN com as tabelas Departamentos (à esquerda) e Funcionários (direita) para selecionar todos os departamentos, inclusive aqueles que não têm funcionários atribuídos a eles. Para selecionar todos os funcionários, inclusive aqueles que não estão atribuídos a um departamento, você usaria RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="a716d-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="a716d-p105">O exemplo a seguir mostra como você pode unir as tabelas Categorias e Produtos no campo ID de Categoria: A consulta produz uma lista de todas as categorias, inclusive aquelas que não contêm produtos:</span><span class="sxs-lookup"><span data-stu-id="a716d-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="a716d-126">Neste exemplo, CategoryID é o campo unido, mas não é incluído nos resultados da consulta porque não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a716d-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="a716d-127">Para incluir o campo unido, insira o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="a716d-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="a716d-128">Para criar uma consulta que inclua somente registros nos quais os dados dos campos unidos sejam iguais, use uma operação [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a716d-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="a716d-p107">Uma LEFT JOIN ou RIGHT JOIN pode estar aninhada em uma INNER JOIN, mas INNER JOIN não pode estar aninhada em uma LEFT JOIN ou RIGHT JOIN. Veja a discussão de aninhamento no tópico INNER JOIN para ver como aninhar junções dentro de outras junções.</span><span class="sxs-lookup"><span data-stu-id="a716d-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="a716d-131">Você pode vincular várias cláusulas ON.</span><span class="sxs-lookup"><span data-stu-id="a716d-131">You can link multiple ON clauses.</span></span> <span data-ttu-id="a716d-132">Veja a discussão sobre vinculação de cláusula no tópico INNER JOIN para ver como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="a716d-132">See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="a716d-133">Se você tentar inserir campos com dados de Memorando ou Objeto OLE, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="a716d-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="a716d-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a716d-134">Example</span></span>

<span data-ttu-id="a716d-135">Este exemplo:</span><span class="sxs-lookup"><span data-stu-id="a716d-135">This is an example.</span></span>
- <span data-ttu-id="a716d-136">Pressupõe a existência de campos de Nomes de Departamento e IDs de departamento hipotéticos em uma tabela de Funcionários.</span><span class="sxs-lookup"><span data-stu-id="a716d-136">This example assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="a716d-137">Observe que esses campos, na verdade, não existem na tabela de Funcionários do banco de dados do Northwind.</span><span class="sxs-lookup"><span data-stu-id="a716d-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="a716d-138">Seleciona todos os departamentos, inclusive os que não têm os funcionários.</span><span class="sxs-lookup"><span data-stu-id="a716d-138">This example selects all departments, including those without employees.</span></span>

- <span data-ttu-id="a716d-139">Chama um procedimento EnumFields, que pode ser encontrado no exemplo de declaração SELECT.</span><span class="sxs-lookup"><span data-stu-id="a716d-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.

</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```

---
title: Operações LEFT JOIN, RIGHT JOIN (SQL do Microsoft Access)
TOCTitle: LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
ms.openlocfilehash: 4e2c9f8b47622bf9408d02b683af4e48d52c8662
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870524"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="e0d39-102">Operações LEFT JOIN, RIGHT JOIN (SQL do Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="e0d39-102">LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="e0d39-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0d39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0d39-104">Combina registros da tabela de origem quando usados em qualquer cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e0d39-104">Combines source-table records when used in any [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0d39-105">Syntax</span></span>

<span data-ttu-id="e0d39-106">DA *tabela 1* \[ esquerda | DIREITA \] JOIN *Tabela2* em *table1.field1* *compopr table2.field2*</span><span class="sxs-lookup"><span data-stu-id="e0d39-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="e0d39-107">As operações LEFT JOIN e RIGHT JOIN têm estas partes:</span><span class="sxs-lookup"><span data-stu-id="e0d39-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0d39-108">Parte</span><span class="sxs-lookup"><span data-stu-id="e0d39-108">Part</span></span></p></th>
<th><p><span data-ttu-id="e0d39-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0d39-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0d39-110"><em>tabela1</em>, <em>compopr2</em></span><span class="sxs-lookup"><span data-stu-id="e0d39-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="e0d39-111">Os nomes das tabelas nas quais os registros são combinados.</span><span class="sxs-lookup"><span data-stu-id="e0d39-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0d39-112"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="e0d39-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="e0d39-p101">Os nomes dos campos unidos. Os campos devem ser do mesmo tipo de dados e conter o mesmo tipo de dados, mas não precisam ter o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="e0d39-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0d39-115"><em>compopr</em></span><span class="sxs-lookup"><span data-stu-id="e0d39-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="e0d39-116">Qualquer operador de comparação relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; ou &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="e0d39-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e0d39-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0d39-117">Remarks</span></span>

<span data-ttu-id="e0d39-p102">Use a operação LEFT JOIN para criar uma junção externa esquerda. As junções externas esquerdas incluem todos os registros da primeira de duas tabelas (a da esquerda), mesmo se não houver valores correspondentes na segunda tabela (à direita).</span><span class="sxs-lookup"><span data-stu-id="e0d39-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="e0d39-p103">Use uma operação RIGHT JOIN para criar uma junção externa direita. As junções externas direitas incluem todos os registros da segunda de duas tabelas (a da direita), mesmo se não houver valores correspondentes para registros na primeira tabela (à esquerda).</span><span class="sxs-lookup"><span data-stu-id="e0d39-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="e0d39-p104">Por exemplo, você poderia usar LEFT JOIN com as tabelas Departamentos (esquerda) e Funcionários (direita) para selecionar todos os departamentos, incluindo os que não tiverem funcionários atribuídos a eles. Para selecionar todos os funcionários, incluindo os não atribuídos a um departamento, você usaria RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="e0d39-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="e0d39-p105">O exemplo a seguir mostra como você poderia unir as tabelas Categorias e Produtos no campo CategoryID. A consulta produz uma lista de todas as categorias, incluindo as que não contêm produtos:</span><span class="sxs-lookup"><span data-stu-id="e0d39-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="e0d39-126">Neste exemplo, CategoryID é o campo unido, mas não é incluído nos resultados da consulta porque não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="e0d39-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="e0d39-127">Para incluir o campo associado, digite o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="e0d39-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="e0d39-128">[!OBSERVAçãO] Para criar uma consulta que inclua somente registros nos quais os dados dos campos unidos sejam iguais, use uma operação [INNER JOIN](inner-join-operation-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="e0d39-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="e0d39-p107">Uma LEFT JOIN ou uma RIGHT JOIN podem ser aninhadas em uma INNER JOIN, mas uma INNER JOIN não pode ser aninhada em uma LEFT JOIN ou em uma RIGHT JOIN. Consulte a discussão sobre aninhamento no tópico sobre INNER JOIN para saber como aninhar junções em outras junções.</span><span class="sxs-lookup"><span data-stu-id="e0d39-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="e0d39-p108">Você pode vincular várias cláusulas ON. Consulte a discussão sobre vinculação de cláusulas no tópico sobre INNER JOIN para ver como isso é feito.</span><span class="sxs-lookup"><span data-stu-id="e0d39-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="e0d39-133">Se você tentar juntar campos contendo dados de objeto OLE ou Memorando, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="e0d39-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="e0d39-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e0d39-134">Example</span></span>

<span data-ttu-id="e0d39-135">Este exemplo:</span><span class="sxs-lookup"><span data-stu-id="e0d39-135">This example:</span></span>
- <span data-ttu-id="e0d39-136">Considera a existência de campos de nome de departamento e a identificação do departamento hipotéticos em uma tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="e0d39-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="e0d39-137">Observe que esses campos não existem realmente na tabela Funcionários do banco de dados da Northwind.</span><span class="sxs-lookup"><span data-stu-id="e0d39-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="e0d39-138">Seleciona todos os departamentos, incluindo aqueles sem funcionários.</span><span class="sxs-lookup"><span data-stu-id="e0d39-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="e0d39-139">Chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="e0d39-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


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

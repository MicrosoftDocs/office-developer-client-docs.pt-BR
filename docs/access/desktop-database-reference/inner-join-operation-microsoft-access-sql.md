---
title: Operação INNER JOIN (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6ff2ad40d318801ecec2332b53b41f327c20fbc5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722519"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="6d5b2-102">Operação INNER JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6d5b2-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="6d5b2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d5b2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6d5b2-104">Combina registros de duas tabelas, sempre que houver valores correspondentes em um campo comum.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d5b2-105">Syntax</span></span>

<span data-ttu-id="6d5b2-106">DA *tabela 1* INNER JOIN *Tabela2* na *tabela 1*. *field1* *compopr Tabela2*. *Field2*</span><span class="sxs-lookup"><span data-stu-id="6d5b2-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="6d5b2-107">A operação INNER JOIN contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="6d5b2-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d5b2-108">Parte</span><span class="sxs-lookup"><span data-stu-id="6d5b2-108">Part</span></span></p></th>
<th><p><span data-ttu-id="6d5b2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d5b2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d5b2-110"><em>tabela1</em>, <em>compopr2</em></span><span class="sxs-lookup"><span data-stu-id="6d5b2-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="6d5b2-111">Os nomes das tabelas nas quais os registros são combinados.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d5b2-112"><em>campo1</em>, <em>campo2</em></span><span class="sxs-lookup"><span data-stu-id="6d5b2-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="6d5b2-p101">Os nomes dos campos unidos. Caso não sejam numéricos, os campos deverão ser do mesmo tipo e conter o mesmo tipo de dados, mas não é necessário que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d5b2-115"><em>compopr</em></span><span class="sxs-lookup"><span data-stu-id="6d5b2-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="6d5b2-116">Qualquer operador de comparação relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; ou &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="6d5b2-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6d5b2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d5b2-117">Remarks</span></span>

<span data-ttu-id="6d5b2-p102">É possível usar uma operação INNER JOIN em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Esse é o tipo de junção mais comum. As junções internas combinam registros de duas tabelas sempre que houver correspondência de valores em campos comuns nas duas tabelas.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="6d5b2-p103">É possível usar a INNER JOIN nas tabelas Departamentos e Funcionários para selecionar todos os funcionários de um departamento. Em contrapartida, para selecionar todos os departamentos (mesmo se não houver funcionários atribuídos a eles) todos os funcionários (mesmo que alguns não estejam atribuídos ao departamento), é possível usar uma operação [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para criar uma junção externa.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="6d5b2-123">Se você tentar juntar campos contendo dados de objeto OLE ou Memorando, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="6d5b2-p104">É possível juntar pares de campos numéricos ou de tipos semelhantes. Por exemplo, você poderá juntar os campos Numeração Automática e Longo, pois eles são de tipos semelhantes. No entanto, não é possível juntar campos de tipo simples com duplos.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="6d5b2-127">O seguinte exemplo mostra como você poderá unir as tabelas Categorias e Produtos no campo CategoryID:</span><span class="sxs-lookup"><span data-stu-id="6d5b2-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="6d5b2-128">No exemplo anterior, CategoryID é o campo associado, mas não está incluído na saída da consulta porque ele não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="6d5b2-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="6d5b2-129">Para incluir o campo associado, inclua o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="6d5b2-130">é possível juntar também diversas cláusulas ON em uma instrução de JUNÇÃO, usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6d5b2-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="6d5b2-131">Selecione os *campos* da *tabela 1* INNER JOIN de Diante *Tabela2* *tabela 1*. *field1* *compopr* *Tabela2*. *field1* E, na *tabela 1*. *Field2* *compopr* *Tabela2*. *field2*) OU, na *tabela 1*. *Field3* *compopr* *Tabela2*. *field3*) \];</span><span class="sxs-lookup"><span data-stu-id="6d5b2-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND ON *table1*.*field2* *compopr* *table2*.*field2*) OR ON *table1*.*field3* *compopr* *table2*.*field3*)\];</span></span>

<span data-ttu-id="6d5b2-132">É possível também aninhar instruções JOIN utilizando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6d5b2-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="6d5b2-133">Selecione os *campos* da *tabela 1* INNER JOIN (*Tabela2* INNER JOIN \[( \] *Tabela3* \[INNER JOIN \[( \] *tablex* \[INNER JOIN...) \] Em *Tabela3*. *Field3* *compopr* *tablex*. *fieldx*) \] Em *Tabela2*. *Field2* *compopr* *Tabela3*. *field3*) NA *tabela 1*. *field1* *compopr* *Tabela2*. *field2*;</span><span class="sxs-lookup"><span data-stu-id="6d5b2-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="6d5b2-134">Uma LEFT JOIN ou uma RIGHT JOIN poderá ser aninhada dentro de uma INNER JOIN, mas a INNER JOIN não poderá ser aninhada dentro de uma LEFT JOIN ou de uma RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="6d5b2-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6d5b2-135">Example</span></span>

<span data-ttu-id="6d5b2-p106">Esse exemplo cria duas equijunções: uma entre as tabelas Pedidos e Detalhes do Pedido, e outra entre as tabelas Pedidos e Funcionários. Isso é necessário, pois a tabela Funcionários não inclui os dados de vendas e a tabela Detalhes do Pedido não inclui dados de funcionários. A consulta vai criar uma lista de funcionários e o total de suas vendas.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="6d5b2-139">Este exemplo chama o procedimento EnumFields, que pode ser localizado no exemplo da instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="6d5b2-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```

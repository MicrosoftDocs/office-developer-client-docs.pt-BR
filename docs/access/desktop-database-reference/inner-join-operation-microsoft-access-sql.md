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
ms.openlocfilehash: d865d005604ed7422c8e33ff8508551b720c30ba
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734214"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="62fb5-102">Operação INNER JOIN (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="62fb5-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="62fb5-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62fb5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="62fb5-104">Combina registros de duas tabelas sempre que houver valores correspondentes em um campo comum.</span><span class="sxs-lookup"><span data-stu-id="62fb5-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="62fb5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62fb5-105">Syntax</span></span>

<span data-ttu-id="62fb5-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span><span class="sxs-lookup"><span data-stu-id="62fb5-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="62fb5-107">A operação INNER JOIN contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="62fb5-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62fb5-108">Parte</span><span class="sxs-lookup"><span data-stu-id="62fb5-108">Part</span></span></p></th>
<th><p><span data-ttu-id="62fb5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="62fb5-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62fb5-110"><em>tabela1</em>, <em>tabela2</em></span><span class="sxs-lookup"><span data-stu-id="62fb5-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="62fb5-111">Os nomes das tabelas das quais os registros são combinados.</span><span class="sxs-lookup"><span data-stu-id="62fb5-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="62fb5-112"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="62fb5-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="62fb5-p101">Os nomes dos campos unidos. Caso não sejam numéricos, os campos deverão ser do mesmo tipo e conter o mesmo tipo de dados, mas não é necessário que tenham o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="62fb5-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="62fb5-115"><em>oprcomp</em></span><span class="sxs-lookup"><span data-stu-id="62fb5-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="62fb5-116">Qualquer operador de comparação relacional: &quot;=&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=&quot; &quot; &gt; =&quot; ou &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="62fb5-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="62fb5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="62fb5-117">Remarks</span></span>

<span data-ttu-id="62fb5-p102">É possível usar uma operação INNER JOIN em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Esse é o tipo de junção mais comum. As junções internas combinam registros de duas tabelas sempre que houver correspondência de valores em campos comuns nas duas tabelas.</span><span class="sxs-lookup"><span data-stu-id="62fb5-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="62fb5-p103">É possível usar a INNER JOIN nas tabelas Departamentos e Funcionários para selecionar todos os funcionários de um departamento. Em contrapartida, para selecionar todos os departamentos (mesmo se não houver funcionários atribuídos a eles) todos os funcionários (mesmo que alguns não estejam atribuídos ao departamento), é possível usar uma operação [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para criar uma junção externa.</span><span class="sxs-lookup"><span data-stu-id="62fb5-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="62fb5-123">Se você tentar inserir campos com dados de Memorando ou Objeto OLE, ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="62fb5-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="62fb5-p104">Você pode juntar quaisquer dois campos numéricos de tipos semelhantes. Por exemplo, você pode juntar os campos Numeração Automática e Longo porque eles são tipos semelhantes. No entanto, você não pode juntar os tipos de campos Único e Duplo.</span><span class="sxs-lookup"><span data-stu-id="62fb5-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="62fb5-127">O exemplo a seguir mostra como você pode unir as tabelas Categorias e Produtos no campo ID de Categoria:</span><span class="sxs-lookup"><span data-stu-id="62fb5-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="62fb5-128">No exemplo anterior, a ID de Categoria é o campo de junção, mas não é incluída na saída de consulta porque não está incluída na instrução [SELECT](select-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="62fb5-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="62fb5-129">Para incluir o campo de junção, insira o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="62fb5-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="62fb5-130">Você também pode vincular várias cláusulas ON em uma instrução de JOIN, usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="62fb5-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="62fb5-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span><span class="sxs-lookup"><span data-stu-id="62fb5-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span></span>

<span data-ttu-id="62fb5-132">Também é possível aninhar instruções JOIN usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="62fb5-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="62fb5-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span><span class="sxs-lookup"><span data-stu-id="62fb5-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="62fb5-134">Uma LEFT JOIN ou RIGHT JOIN pode estar aninhada em uma INNER JOIN, mas INNER JOIN não pode estar aninhada dentro de uma LEFT JOIN ou RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="62fb5-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="62fb5-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="62fb5-135">Example</span></span>

<span data-ttu-id="62fb5-p106">Esse exemplo cria duas equijunções: uma entre as tabelas Pedidos e Detalhes do Pedido, e outra entre as tabelas Pedidos e Funcionários. Isso é necessário, pois a tabela Funcionários não inclui os dados de vendas e a tabela Detalhes do Pedido não inclui dados de funcionários. A consulta vai criar uma lista de funcionários e o total de suas vendas.</span><span class="sxs-lookup"><span data-stu-id="62fb5-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="62fb5-139">Este exemplo chama o procedimento EnumFields, que você pode encontrar no exemplo de instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="62fb5-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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

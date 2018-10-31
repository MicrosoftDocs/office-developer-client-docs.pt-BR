---
title: TRANSFORMAR instrução (Microsoft Access SQL)
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 16b88f2cf441802c6246425d5bb7bb2efb71a679
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861215"
---
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="76341-102">TRANSFORMAR instrução (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="76341-102">TRANSFORM statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="76341-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="76341-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="76341-104">Cria uma consulta de tabela de referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="76341-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="76341-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76341-105">Syntax</span></span>

<span data-ttu-id="76341-106">TRANSFORMAR *aggfunctionselectstatement* PIVOT *pivotfield* \[pol (*valor1*\[, *value2*\[,... \]\])\]</span><span class="sxs-lookup"><span data-stu-id="76341-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="76341-107">A instrução TRANSFORM contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="76341-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="76341-108">Parte</span><span class="sxs-lookup"><span data-stu-id="76341-108">Part</span></span></p></th>
<th><p><span data-ttu-id="76341-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="76341-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="76341-110"><em>aggfunction</em></span><span class="sxs-lookup"><span data-stu-id="76341-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="76341-111">Uma <a href="sql-aggregate-functions-sql.md">função de agregação de SQL</a> que funciona em dados selecionados.</span><span class="sxs-lookup"><span data-stu-id="76341-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76341-112"><em>selectstatement</em></span><span class="sxs-lookup"><span data-stu-id="76341-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="76341-113">Uma instrução <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="76341-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="76341-114"><em>pivotfield</em></span><span class="sxs-lookup"><span data-stu-id="76341-114"><em>pivotfield</em></span></span></p></td>
<td><p><span data-ttu-id="76341-115">O campo ou expressão que deseja usar para criar títulos de colunas no conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="76341-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="76341-116"><em>value1</em>, <em>value2</em></span><span class="sxs-lookup"><span data-stu-id="76341-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="76341-117">Valores fixos usados para criar títulos de colunas.</span><span class="sxs-lookup"><span data-stu-id="76341-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="76341-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="76341-118">Remarks</span></span>

<span data-ttu-id="76341-119">Ao resumir dados utilizando uma consulta de tabela de referência cruzada, você seleciona valores de campos ou expressões especificados como títulos de colunas para que seja possível exibir dados em um formato mais compacto do que o formato da consulta de seleção.</span><span class="sxs-lookup"><span data-stu-id="76341-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="76341-p101">TRANSFORM é opcional, mas, quando incluso, é a primeira instrução em uma sequência SQL. Ela precede uma instrução SELECT que especifica os campos utilizados como títulos de linha e uma cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) que especifica o agrupamento de linhas. Opcionalmente, você pode incluir outras cláusulas, como [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), que especifica critérios adicionais de seleção ou classificação. Você também pode usar subconsultas como predicados  especificamente, aqueles na cláusula WHERE  em uma consulta de tabela de referência cruzada.</span><span class="sxs-lookup"><span data-stu-id="76341-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="76341-p102">Os valores retornados em *pivotfield* são utilizados como títulos de colunas no conjunto de resultados da consulta. Por exemplo, dinamizar as figuras de vendas no mês de vendas, em um consulta de tabela de referência cruzada cria 12 colunas. Você pode restringir *pivotfield* para criar títulos de valores fixos (*value1*, *value2* ) listados na cláusula IN opcional. Também é possível incluir valores fixos que não têm nenhum dado para criar colunas adicionais.</span><span class="sxs-lookup"><span data-stu-id="76341-p102">The values returned in *pivotfield* are used as column headings in the query's result set. For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns. You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause. You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="76341-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76341-128">Example</span></span>

<span data-ttu-id="76341-p103">Este exemplo usa a cláusula SQL TRANSFORM para criar uma consulta entre guias, mostrando o número de pedidos feitos por cada cliente em cada trimestre de 1994. A função SQLTRANSFORMOutput é necessária para a execução desse procedimento.</span><span class="sxs-lookup"><span data-stu-id="76341-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="76341-p104">Este exemplo usa a cláusula SQL TRANSFORM para criar uma consulta entre guias um pouco mais complexa, mostrando o valor total em dólar dos pedidos feitos por cada cliente em cada trimestre de 1994. A função SQLTRANSFORMOutput é necessária para a execução desse procedimento.</span><span class="sxs-lookup"><span data-stu-id="76341-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```

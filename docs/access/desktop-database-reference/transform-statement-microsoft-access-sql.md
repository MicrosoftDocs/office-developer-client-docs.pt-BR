---
title: Instrução TRANSFORM (Microsoft Access SQL)
TOCTitle: TRANSFORM Statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d05f278e38cc8cf132cf06605703dfa99eb8728
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464394"
---
# <a name="transform-statement-microsoft-access-sql"></a>Instrução TRANSFORM (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Cria uma consulta de tabela de referência cruzada.

## <a name="syntax"></a>Sintaxe

TRANSFORMAR *aggfunctionselectstatement* PIVOT *pivotfield* \[pol (*valor1*\[, *value2*\[,... \]\])\]

A instrução TRANSFORM contém estas partes:

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
<td><p><em>aggfunction</em></p></td>
<td><p>Uma <a href="sql-aggregate-functions-sql.md">função de agregação de SQL</a> que funciona em dados selecionados.</p></td>
</tr>
<tr class="even">
<td><p><em>selectstatement</em></p></td>
<td><p>Uma instrução <a href="select-statement-microsoft-access-sql.md">SELECT</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>pivotfield</em></p></td>
<td><p>O campo ou expressão que deseja usar para criar títulos de colunas no conjunto de resultados da consulta.</p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>, <em>value2</em></p></td>
<td><p>Valores fixos usados para criar títulos de colunas.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

Ao resumir dados utilizando uma consulta de tabela de referência cruzada, você seleciona valores de campos ou expressões especificados como títulos de colunas para que seja possível exibir dados em um formato mais compacto do que o formato da consulta de seleção.

TRANSFORM é opcional, mas, quando incluso, é a primeira instrução em uma sequência SQL. Ela precede uma instrução SELECT que especifica os campos utilizados como títulos de linha e uma cláusula [GROUP BY](https://msdn.microsoft.com/library/ff837271\(v=office.15\)) que especifica o agrupamento de linhas. Opcionalmente, você pode incluir outras cláusulas, como [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)), que especifica critérios adicionais de seleção ou classificação. Você também pode usar subconsultas como predicados  especificamente, aqueles na cláusula WHERE  em uma consulta de tabela de referência cruzada.

Os valores retornados em *pivotfield* são utilizados como títulos de colunas no conjunto de resultados da consulta. Por exemplo, dinamizar as figuras de vendas no mês de vendas, em um consulta de tabela de referência cruzada cria 12 colunas. Você pode restringir *pivotfield* para criar títulos de valores fixos (*value1*, *value2* ) listados na cláusula IN opcional. Também é possível incluir valores fixos que não têm nenhum dado para criar colunas adicionais.

## <a name="example"></a>Exemplo

Este exemplo usa a cláusula SQL TRANSFORM para criar uma consulta entre guias, mostrando o número de pedidos feitos por cada cliente em cada trimestre de 1994. A função SQLTRANSFORMOutput é necessária para a execução desse procedimento.

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

Este exemplo usa a cláusula SQL TRANSFORM para criar uma consulta entre guias um pouco mais complexa, mostrando o valor total em dólar dos pedidos feitos por cada cliente em cada trimestre de 1994. A função SQLTRANSFORMOutput é necessária para a execução desse procedimento.

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

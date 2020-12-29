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
# <a name="inner-join-operation-microsoft-access-sql"></a>Operação INNER JOIN (Microsoft Access SQL)


**Aplica-se ao:** Access 2013, Office 2013


Combina registros de duas tabelas sempre que houver valores correspondentes em um campo comum.

## <a name="syntax"></a>Sintaxe

FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*

A operação INNER JOIN contém as seguintes partes:

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
<td><p><em>tabela1</em>, <em>tabela2</em></p></td>
<td><p>Os nomes das tabelas das quais os registros são combinados.</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>Os nomes dos campos unidos. Caso não sejam numéricos, os campos deverão ser do mesmo tipo e conter o mesmo tipo de dados, mas não é necessário que tenham o mesmo nome.</p></td>
</tr>
<tr class="odd">
<td><p><em>oprcomp</em></p></td>
<td><p>Qualquer operador de comparação relacional: &quot;=&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=&quot; &quot; &gt; =&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

É possível usar uma operação INNER JOIN em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql). Esse é o tipo de junção mais comum. As junções internas combinam registros de duas tabelas sempre que houver correspondência de valores em campos comuns nas duas tabelas.

É possível usar a INNER JOIN nas tabelas Departamentos e Funcionários para selecionar todos os funcionários de um departamento. Em contrapartida, para selecionar todos os departamentos (mesmo se não houver funcionários atribuídos a eles) todos os funcionários (mesmo que alguns não estejam atribuídos ao departamento), é possível usar uma operação [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para criar uma junção externa.

Se você tentar inserir campos com dados de Memorando ou Objeto OLE, ocorrerá um erro.

Você pode juntar quaisquer dois campos numéricos de tipos semelhantes. Por exemplo, você pode juntar os campos Numeração Automática e Longo porque eles são tipos semelhantes. No entanto, você não pode juntar os tipos de campos Único e Duplo.

O exemplo a seguir mostra como você pode unir as tabelas Categorias e Produtos no campo ID de Categoria:

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

No exemplo anterior, a ID de Categoria é o campo de junção, mas não é incluída na saída de consulta porque não está incluída na instrução [SELECT](select-statement-microsoft-access-sql.md). Para incluir o campo de junção, insira o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.

Você também pode vincular várias cláusulas ON em uma instrução de JOIN, usando a seguinte sintaxe:

SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;

Também é possível aninhar instruções JOIN usando a seguinte sintaxe:

SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;

Uma LEFT JOIN ou RIGHT JOIN pode estar aninhada em uma INNER JOIN, mas INNER JOIN não pode estar aninhada dentro de uma LEFT JOIN ou RIGHT JOIN.

## <a name="example"></a>Exemplo

Esse exemplo cria duas equijunções: uma entre as tabelas Pedidos e Detalhes do Pedido, e outra entre as tabelas Pedidos e Funcionários. Isso é necessário, pois a tabela Funcionários não inclui os dados de vendas e a tabela Detalhes do Pedido não inclui dados de funcionários. A consulta vai criar uma lista de funcionários e o total de suas vendas.

Este exemplo chama o procedimento EnumFields, que você pode encontrar no exemplo de instrução SELECT.

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

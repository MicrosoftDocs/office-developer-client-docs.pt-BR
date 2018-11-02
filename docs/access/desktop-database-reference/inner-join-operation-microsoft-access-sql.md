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
ms.openlocfilehash: 4f9593e8bf0175ee6a25bd53d886c291eed6f75c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929431"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>Operação INNER JOIN (Microsoft Access SQL)


**Aplica-se a**: Access 2013, o Office 2013


Combina registros de duas tabelas, sempre que houver valores correspondentes em um campo comum.

## <a name="syntax"></a>Sintaxe

DA *tabela 1* INNER JOIN *Tabela2* na *tabela 1*. *field1* *compopr Tabela2*. *Field2*

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
<td><p><em>tabela1</em>, <em>compopr2</em></p></td>
<td><p>Os nomes das tabelas nas quais os registros são combinados.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Os nomes dos campos unidos. Caso não sejam numéricos, os campos deverão ser do mesmo tipo e conter o mesmo tipo de dados, mas não é necessário que tenham o mesmo nome.</p></td>
</tr>
<tr class="odd">
<td><p><em>compopr</em></p></td>
<td><p>Qualquer operador de comparação relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

É possível usar uma operação INNER JOIN em qualquer cláusula [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)). Esse é o tipo de junção mais comum. As junções internas combinam registros de duas tabelas sempre que houver correspondência de valores em campos comuns nas duas tabelas.

É possível usar a INNER JOIN nas tabelas Departamentos e Funcionários para selecionar todos os funcionários de um departamento. Em contrapartida, para selecionar todos os departamentos (mesmo se não houver funcionários atribuídos a eles) todos os funcionários (mesmo que alguns não estejam atribuídos ao departamento), é possível usar uma operação [LEFT JOIN ou RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) para criar uma junção externa.

Se você tentar juntar campos contendo dados de objeto OLE ou Memorando, ocorrerá um erro.

É possível juntar pares de campos numéricos ou de tipos semelhantes. Por exemplo, você poderá juntar os campos Numeração Automática e Longo, pois eles são de tipos semelhantes. No entanto, não é possível juntar campos de tipo simples com duplos.

O seguinte exemplo mostra como você poderá unir as tabelas Categorias e Produtos no campo CategoryID:

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

No exemplo anterior, CategoryID é o campo associado, mas não está incluído na saída da consulta porque ele não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md) . Para incluir o campo associado, inclua o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.

é possível juntar também diversas cláusulas ON em uma instrução de JUNÇÃO, usando a seguinte sintaxe:

Selecione os *campos* da *tabela 1* INNER JOIN de Diante *Tabela2* *tabela 1*. *field1* *compopr* *Tabela2*. *field1* E, na *tabela 1*. *Field2* *compopr* *Tabela2*. *field2*) OU, na *tabela 1*. *Field3* *compopr* *Tabela2*. *field3*) \];

É possível também aninhar instruções JOIN utilizando a seguinte sintaxe:

Selecione os *campos* da *tabela 1* INNER JOIN (*Tabela2* INNER JOIN \[( \] *Tabela3* \[INNER JOIN \[( \] *tablex* \[INNER JOIN...) \] Em *Tabela3*. *Field3* *compopr* *tablex*. *fieldx*) \] Em *Tabela2*. *Field2* *compopr* *Tabela3*. *field3*) NA *tabela 1*. *field1* *compopr* *Tabela2*. *field2*;

Uma LEFT JOIN ou uma RIGHT JOIN poderá ser aninhada dentro de uma INNER JOIN, mas a INNER JOIN não poderá ser aninhada dentro de uma LEFT JOIN ou de uma RIGHT JOIN.

## <a name="example"></a>Exemplo

Esse exemplo cria duas equijunções: uma entre as tabelas Pedidos e Detalhes do Pedido, e outra entre as tabelas Pedidos e Funcionários. Isso é necessário, pois a tabela Funcionários não inclui os dados de vendas e a tabela Detalhes do Pedido não inclui dados de funcionários. A consulta vai criar uma lista de funcionários e o total de suas vendas.

Este exemplo chama o procedimento EnumFields, que pode ser localizado no exemplo da instrução SELECT.

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

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
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>Operações LEFT JOIN RIGHT JOIN (SQL do Microsoft Access)

**Aplica-se ao:** Access 2013, Office 2013

Combina registros da tabela de origem quando usados em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxe

FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*

As operações LEFT JOIN e RIGHT JOIN têm estas partes:

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
<td><p>Os nomes dos campos unidos. Os campos devem ser do mesmo tipo de dados e conter o mesmo tipo de dados, mas não precisam ter o mesmo nome.</p></td>
</tr>
<tr class="odd">
<td><p><em>oprcomp</em></p></td>
<td><p>Qualquer operador de comparação relacional: &quot;=&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=&quot; &quot; &gt; =&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a operação LEFT JOIN para criar uma junção externa esquerda. As junções externas esquerdas incluem todos os registros da primeira de duas tabelas (a da esquerda), mesmo se não houver valores correspondentes na segunda tabela (à direita).

Use uma operação RIGHT JOIN para criar uma junção externa direita. As junções externas direitas incluem todos os registros da segunda de duas tabelas (a da direita), mesmo se não houver valores correspondentes para registros na primeira tabela (à esquerda).

Por exemplo, você poderia usar LEFT JOIN com as tabelas Departamentos (à esquerda) e Funcionários (direita) para selecionar todos os departamentos, inclusive aqueles que não têm funcionários atribuídos a eles. Para selecionar todos os funcionários, inclusive aqueles que não estão atribuídos a um departamento, você usaria RIGHT JOIN.

O exemplo a seguir mostra como você pode unir as tabelas Categorias e Produtos no campo ID de Categoria: A consulta produz uma lista de todas as categorias, inclusive aquelas que não contêm produtos:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Neste exemplo, CategoryID é o campo unido, mas não é incluído nos resultados da consulta porque não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md). Para incluir o campo unido, insira o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.

> [!NOTE]
> - Para criar uma consulta que inclua somente registros nos quais os dados dos campos unidos sejam iguais, use uma operação [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Uma LEFT JOIN ou RIGHT JOIN pode estar aninhada em uma INNER JOIN, mas INNER JOIN não pode estar aninhada em uma LEFT JOIN ou RIGHT JOIN. Veja a discussão de aninhamento no tópico INNER JOIN para ver como aninhar junções dentro de outras junções.
> - Você pode vincular várias cláusulas ON. Veja a discussão sobre vinculação de cláusula no tópico INNER JOIN para ver como fazer isso.
> - Se você tentar inserir campos com dados de Memorando ou Objeto OLE, ocorrerá um erro.

## <a name="example"></a>Exemplo

Este exemplo:
- Pressupõe a existência de campos de Nomes de Departamento e IDs de departamento hipotéticos em uma tabela de Funcionários. Observe que esses campos, na verdade, não existem na tabela de Funcionários do banco de dados do Northwind.

- Seleciona todos os departamentos, inclusive os que não têm os funcionários.

- Chama um procedimento EnumFields, que pode ser encontrado no exemplo de declaração SELECT.


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

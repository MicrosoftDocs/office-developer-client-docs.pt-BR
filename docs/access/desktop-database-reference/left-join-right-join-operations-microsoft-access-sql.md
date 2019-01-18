---
title: LEFT JOIN, RIGHT JOIN operações (Microsoft Access SQL)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704718"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN, RIGHT JOIN operações (Microsoft Access SQL)

**Aplica-se a**: Access 2013, o Office 2013

Combina registros da tabela de origem quando usados em qualquer cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxe

DA *tabela 1* \[ esquerda | DIREITA \] JOIN *Tabela2* em *table1.field1* *compopr table2.field2*

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
<td><p><em>tabela1</em>, <em>compopr2</em></p></td>
<td><p>Os nomes das tabelas nas quais os registros são combinados.</p></td>
</tr>
<tr class="even">
<td><p><em>campo1</em>, <em>campo2</em></p></td>
<td><p>Os nomes dos campos unidos. Os campos devem ser do mesmo tipo de dados e conter o mesmo tipo de dados, mas não precisam ter o mesmo nome.</p></td>
</tr>
<tr class="odd">
<td><p><em>compopr</em></p></td>
<td><p>Qualquer operador de comparação relacional: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; ou &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Use a operação LEFT JOIN para criar uma junção externa esquerda. As junções externas esquerdas incluem todos os registros da primeira de duas tabelas (a da esquerda), mesmo se não houver valores correspondentes na segunda tabela (à direita).

Use uma operação RIGHT JOIN para criar uma junção externa direita. As junções externas direitas incluem todos os registros da segunda de duas tabelas (a da direita), mesmo se não houver valores correspondentes para registros na primeira tabela (à esquerda).

Por exemplo, você poderia usar LEFT JOIN com as tabelas Departamentos (esquerda) e Funcionários (direita) para selecionar todos os departamentos, incluindo os que não tiverem funcionários atribuídos a eles. Para selecionar todos os funcionários, incluindo os não atribuídos a um departamento, você usaria RIGHT JOIN.

O exemplo a seguir mostra como você poderia unir as tabelas Categorias e Produtos no campo CategoryID. A consulta produz uma lista de todas as categorias, incluindo as que não contêm produtos:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Neste exemplo, CategoryID é o campo unido, mas não é incluído nos resultados da consulta porque não está incluído na instrução [SELECT](select-statement-microsoft-access-sql.md). Para incluir o campo associado, digite o nome do campo na instrução SELECT — neste caso, Categories.CategoryID.

> [!NOTE]
> - [!OBSERVAçãO] Para criar uma consulta que inclua somente registros nos quais os dados dos campos unidos sejam iguais, use uma operação [INNER JOIN](inner-join-operation-microsoft-access-sql.md).
> - Uma LEFT JOIN ou uma RIGHT JOIN podem ser aninhadas em uma INNER JOIN, mas uma INNER JOIN não pode ser aninhada em uma LEFT JOIN ou em uma RIGHT JOIN. Consulte a discussão sobre aninhamento no tópico sobre INNER JOIN para saber como aninhar junções em outras junções.
> - Você pode vincular várias cláusulas ON. Consulte a discussão sobre vinculação de cláusulas no tópico sobre INNER JOIN para ver como isso é feito.
> - Se você tentar juntar campos contendo dados de objeto OLE ou Memorando, ocorrerá um erro.

## <a name="example"></a>Exemplo

Este exemplo:
- Considera a existência de campos de nome de departamento e a identificação do departamento hipotéticos em uma tabela Funcionários. Observe que esses campos não existem realmente na tabela Funcionários do banco de dados da Northwind.

- Seleciona todos os departamentos, incluindo aqueles sem funcionários.

- Chama o procedimento EnumFields, que pode ser encontrado no exemplo da instrução SELECT.


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

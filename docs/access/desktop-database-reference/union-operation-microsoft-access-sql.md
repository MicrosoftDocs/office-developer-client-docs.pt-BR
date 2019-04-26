---
title: Operação UNION (SQL do Microsoft Access)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314697"
---
# <a name="union-operation-microsoft-access-sql"></a>Operação UNION (SQL do Microsoft Access)

**Aplica-se ao:** Access 2013, Office 2013

Cria uma consulta união, que combina os resultados de duas ou mais consultas ou tabelas independentes.

## <a name="syntax"></a>Sintaxe

\[TABLE\] *consulta1* UNION \[ALL\] \[TABLE\] *consulta2* \[UNION \[ALL\] \[TABLE\] *consultan* \[ … \]\]

A operação UNION tem estas partes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Sair</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>consulta1-n</em></p></td>
<td><p>Uma instrução SELECT, o nome de uma consulta armazenada ou o nome de uma tabela armazenada precedida pela palavra-chave TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

É possível mesclar os resultados de duas ou mais consultas, tabelas e instruções SELECT, em qualquer combinação, em uma única operação UNION. O exemplo a seguir mescla uma tabela existente chamada New Accounts e uma instrução SELECT:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Por padrão, nenhum registro duplicado é retornado quando você usa uma operação UNION; contudo, você pode incluir o predicado [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) para garantir que todos os registros sejam retornados. Isso também faz com que a consulta seja executada de modo mais rápido.

Todas as consultas em uma operação UNION devem solicitar o mesmo número de campos; entretanto, os campos não têm que ser do mesmo tamanho nem do mesmo tipo de dados.

Use aliases apenas na primeira instrução SELECT, porque eles são ignorados em quaisquer outras. Na cláusula ORDER BY, faça referência aos campos pelos quais eles são chamados na primeira instrução SELECT.

> [!NOTE]
> - Você pode usar uma cláusula [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) ou [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) em cada argumento *query* para agrupar os dados retornados.
> - Você pode usar uma cláusula [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) no final do último argumento *query* para exibir dados retornados em um ordem específica.

## <a name="example"></a>Exemplo

Este exemplo recupera os nomes e cidades de todos os clientes e fornecedores no Brasil. Ele é chamado procedimento EnumFields, e pode ser encontrado no exemplo da instrução SELECT.

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```

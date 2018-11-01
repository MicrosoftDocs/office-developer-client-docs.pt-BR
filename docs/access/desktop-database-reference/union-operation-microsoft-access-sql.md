---
title: Operação UNION (SQL do Microsoft Access)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 63ff883f35dabbbd69e1bf144eb32016f303c7ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879106"
---
# <a name="union-operation-microsoft-access-sql"></a>Operação UNION (SQL do Microsoft Access)


**Aplica-se a**: Access 2013, o Office 2013

Cria uma consulta união, que combina os resultados de duas ou mais consultas ou tabelas independentes.

## <a name="syntax"></a>Sintaxe

\[TABELA\] *Consulta1* união \[todas as\] \[tabela\] *consulta2* \[união \[todas as\] \[tabela\] *queryn* \[ … \]\]

A operação UNION contém estas partes:

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
<td><p><em>query1-n</em></p></td>
<td><p>Uma instrução SELECT, o nome de uma consulta armazenada ou o nome de uma tabela armazenada precedida pela palavra-chave TABLE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode mesclar os resultados de duas ou mais consultas, tabelas e instruções SELECT, em qualquer combinação, em uma única operação UNION. O exemplo a seguir mescla uma tabela existente chamada Novas Contas e uma instrução SELECT:

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

Por padrão, nenhum registro duplicado é retornado quando você usa uma operação UNION; contudo, você pode incluir o predicado [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) para garantir que todos os registros sejam retornados. Isso também faz com que a consulta seja executada de modo mais rápido.

Todas as consultas em uma operação UNION devem solicitar o mesmo número de campos; entretanto, os campos não têm que ser do mesmo tamanho nem do mesmo tipo de dados.

Use aliases somente na primeira instrução SELECT, porque eles são ignorados em quaisquer outras instruções. Na cláusula ORDER BY, refira-se aos campos pelo modo como são chamados na primeira instrução SELECT.


> [!NOTE]
> <UL>
> <LI>
> <P>Você pode usar uma cláusula <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> ou <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> em cada argumento <EM>query</EM> para agrupar os dados retornados.</P>
> <LI>
> <P>Você pode usar uma cláusula <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> no final do último argumento <EM>query</EM> para exibir os dados retornados em uma ordem específica.</P></LI></UL>



## <a name="example"></a>Exemplo

Este exemplo recupera os nomes e as cidades de todos os fornecedores e clientes no Brasil.

Este exemplo chama o procedimento EnumFields, que pode ser localizado no exemplo da instrução SELECT.

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

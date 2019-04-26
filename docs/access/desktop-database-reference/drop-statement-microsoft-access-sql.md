---
title: Instrução DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293648"
---
# <a name="drop-statement-microsoft-access-sql"></a>Instrução DROP (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Exclui uma tabela, procedimento ou modo de exibição existente de um banco de dados ou exclui um índice existente de uma tabela.

> [!NOTE]
> O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de DROP nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access. Use os métodos **Delete** do ADO no lugar.

## <a name="syntax"></a>Sintaxe

DROP {TABLE *tabela* | INDEX *índice* ON *tabela* | PROCEDURE *procedimento* | VIEW *exibição*}

A instrução DROP tem as seguintes partes:

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
<td><p><em>table</em></p></td>
<td><p>O nome da tabela a ser excluída ou tabela da qual um índice será excluído.</p></td>
</tr>
<tr class="even">
<td><p><em>procedimento</em></p></td>
<td><p>O nome do procedimento a ser excluído.</p></td>
</tr>
<tr class="odd">
<td><p><em>exibição</em></p></td>
<td><p>O nome do modo de exibição a ser excluído.</p></td>
</tr>
<tr class="even">
<td><p><em>índice</em></p></td>
<td><p>O nome do índice a ser excluído da tabela <em>.</em></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você deve fechar a tabela antes de excluir ou remover um índice dela.

Você também pode usar [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para excluir um índice de uma tabela.

Você pode usar [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar uma tabela e [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ou ALTER TABLE para criar um índice. Para modificar uma tabela, use ALTER TABLE.

## <a name="example"></a>Exemplo

O exemplo a seguir considera a existência de um índice NewIndex hipotético na tabela Funcionários no banco de dados Northwind.

Este exemplo exclui o índice MyIndex na tabela Funcionários.

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Este exemplo exclui a tabela Funcionários do banco de dados.

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```

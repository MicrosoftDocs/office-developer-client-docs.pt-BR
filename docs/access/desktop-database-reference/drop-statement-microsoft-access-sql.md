---
title: Instrução DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7622c81e9c37f1fdd2f950c16cd9d8f30caa7cac
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861390"
---
# <a name="drop-statement-microsoft-access-sql"></a>Instrução DROP (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Exclui uma tabela, um procedimento ou uma exibição existente de um banco de dados ou exclui um índice existente de uma tabela.

> [!NOTE]
> [!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de DROP nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access. Use os métodos **Delete** do ADO no lugar.

## <a name="syntax"></a>Sintaxe

DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}

A instrução DROP tem estas partes:

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
<td><p><em>table</em></p></td>
<td><p>O nome da tabela a ser excluída ou a tabela da qual um índice deve ser excluído.</p></td>
</tr>
<tr class="even">
<td><p><em>procedure</em></p></td>
<td><p>O nome do procedimento a ser criado.</p></td>
</tr>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>O nome da exibição a ser excluída.</p></td>
</tr>
<tr class="even">
<td><p><em>índice</em></p></td>
<td><p>O nome do índice a ser excluído da <em>tabela</em>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Para poder remover um índice da tabela ou excluí-la, você deve antes fechá-la.

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

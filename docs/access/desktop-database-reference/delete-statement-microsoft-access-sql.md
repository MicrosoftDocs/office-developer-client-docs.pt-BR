---
title: Instrução DELETE (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a4ef478e74f9851012d6f749e64b4ddb34f3a959
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294040"
---
# <a name="delete-statement-microsoft-access-sql"></a>Instrução DELETE (Microsoft Access SQL)

**Aplica-se ao**: Access 2013, Office 2013

Cria uma consulta de exclusão que remove os registros de uma ou mais tabelas listadas na cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) que atenda à cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).

## <a name="syntax"></a>Sintaxe

DELETE \[*table*.\*\] FROM *table* WHERE *criteria*

A instrução DELETE tem as seguintes partes:

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
<td><p>O nome opcional da tabela da qual os registros são excluídos.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>O nome da tabela da qual os registros são excluídos.</p></td>
</tr>
<tr class="odd">
<td><p><em>critério</em></p></td>
<td><p>Uma expressão que determina quais registros serão excluídos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

DELETE é especialmente útil quando você deseja excluir vários registros.

Para eliminar uma tabela inteira do banco de dados, você pode usar o método **Execute** com uma instrução [DROP](drop-statement-microsoft-access-sql.md). Se você excluir a tabela, contudo, a estrutura será perdida. Do contrário, quando você usar DELETE, somente os dados serão excluídos; a estrutura da tabela e todas as propriedades da tabela, como os atributos e os índices de campos, permanecerão intactos.

Você pode usar DELETE para remover registros das tabelas que estão em uma relação um-para-muitos com outras tabelas. As operações de exclusão em cascata fazem com que os registros nas tabelas, que estão no lado muitos da relação, sejam excluídos quando o registro correspondente no lado um da relação for excluído na consulta. Por exemplo, na relação entre as tabelas Clientes e Pedidos, a tabela Clientes está no lado um e a tabela Pedidos está no lado muito da relação. A exclusão de Clientes resulta na exclusão dos registros correspondentes em Pedidos, se a opção de exclusão em cascata estiver especificada.

Uma consulta de exclusão exclui registros inteiros, não apenas dados em campos específicos. Se você quiser excluir valores em um campo específico, crie uma consulta de atualização que altere os valores para **Null**.

> [!IMPORTANT]
> - Depois de remover registros utilizando uma consulta de exclusão, você não poderá desfazer a operação. Se você quiser saber quais registros foram excluídos, primeiro examine os resultados de uma consulta de seleção que use os mesmos critérios e, em seguida, execute a consulta de exclusão.
> - Mantenha cópias de backup de seus dados em todos os momentos. Se você excluir os registros errados, poderá recuperá-los das cópias de backup.

## <a name="example"></a>Exemplo

Este exemplo exclui todos os registros de funcionários cujo cargo é Trainee. Quando a cláusula FROM inclui apenas uma tabela, não é necessário listar o nome da tabela na instrução DELETE.

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```

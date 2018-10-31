---
title: SELECIONE. EM instrução (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 1c05679994cfd98fdc5d6ffb389df00c2f5c9b94
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861992"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECIONE. EM instrução (Microsoft Access SQL)

**Aplica-se a**: Access 2013 | Office 2013

Cria uma consulta criar tabela.

## <a name="syntax"></a>Sintaxe

Selecione *field1*\[, *field2*\[,... \] \] Em *nova tabela* \[na *externaldatabase* \] da *fonte*

A instrução SELECT... INTO contém estas partes:

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
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>O nome dos campos a serem copiados para a nova tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>newtable</em></p></td>
<td><p>O nome da tabela a ser criada. Ele deve atender às convenções de nomenclatura padrão. Se <em>newtable</em> tiver o mesmo nome de uma tabela existente, ocorrerá um erro interceptável.</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>O caminho para um banco de dados externo. Para obter a descrição do caminho, consulte a cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </p></td>
</tr>
<tr class="even">
<td><p><em>fonte</em></p></td>
<td><p>O nome da tabela existente da qual os registros são selecionados. Pode ser uma ou várias tabelas ou uma consulta.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar as consultas criar tabela para arquivar registros, fazer cópias de backup das tabelas ou fazer cópias para exportar para outros bancos de dados ou para usar como base de relatórios que exibem dados em um determinado período de tempo. Por exemplo, você gerar um relatório Vendas Mensais por Região, executando a mesma consulta criar tabela a cada mês.

> [!NOTE]
> - Talvez você queira definir a chave primária para a nova tabela. Quando você cria a tabela, os campos na nova tabela herdam o tipo de dados e o tamanho do campo para cada campo nas tabelas subjacentes da consulta, mas nenhuma outra propriedade do campo ou da tabela é transferida.
> - Para adicionar dados a uma tabela existente, use a instrução [INSERT INTO](insert-into-statement-microsoft-access-sql.md) em vez de criar uma consulta acréscimo.
> - Para descobrir quais registros serão selecionados antes de executar a consulta criar tabela, primeiro examine os resultados de uma instrução [SELECT](select-statement-microsoft-access-sql.md) que usa os mesmos critérios de seleção.



## <a name="example"></a>Exemplo

Este exemplo seleciona todos os registros na tabela Funcionários e copia-os para uma nova tabela chamada Emp Backup.

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```

---
title: SELECIONE. EM instrução (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: a744f67eba768ac2924d73782dbe70fd57e0333c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885532"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="ba73b-102">SELECIONE. EM instrução (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ba73b-102">SELECT.INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ba73b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba73b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba73b-104">Cria uma consulta criar tabela.</span><span class="sxs-lookup"><span data-stu-id="ba73b-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba73b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba73b-105">Syntax</span></span>

<span data-ttu-id="ba73b-106">Selecione *field1*\[, *field2*\[,... \] \] Em *nova tabela* \[na *externaldatabase* \] da *fonte*</span><span class="sxs-lookup"><span data-stu-id="ba73b-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="ba73b-107">A instrução SELECT... INTO contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="ba73b-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba73b-108">Parte</span><span class="sxs-lookup"><span data-stu-id="ba73b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="ba73b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba73b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba73b-110"><em>field1</em>, <em>field2</em></span><span class="sxs-lookup"><span data-stu-id="ba73b-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="ba73b-111">O nome dos campos a serem copiados para a nova tabela.</span><span class="sxs-lookup"><span data-stu-id="ba73b-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba73b-112"><em>newtable</em></span><span class="sxs-lookup"><span data-stu-id="ba73b-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="ba73b-p101">O nome da tabela a ser criada. Ele deve atender às convenções de nomenclatura padrão. Se <em>newtable</em> tiver o mesmo nome de uma tabela existente, ocorrerá um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="ba73b-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba73b-116"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="ba73b-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="ba73b-p102">O caminho para um banco de dados externo. Para obter a descrição do caminho, consulte a cláusula <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a>.  </span><span class="sxs-lookup"><span data-stu-id="ba73b-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba73b-119"><em>fonte</em></span><span class="sxs-lookup"><span data-stu-id="ba73b-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="ba73b-p103">O nome da tabela existente da qual os registros são selecionados. Pode ser uma ou várias tabelas ou uma consulta.</span><span class="sxs-lookup"><span data-stu-id="ba73b-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ba73b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba73b-122">Remarks</span></span>

<span data-ttu-id="ba73b-p104">Você pode usar as consultas criar tabela para arquivar registros, fazer cópias de backup das tabelas ou fazer cópias para exportar para outros bancos de dados ou para usar como base de relatórios que exibem dados em um determinado período de tempo. Por exemplo, você gerar um relatório Vendas Mensais por Região, executando a mesma consulta criar tabela a cada mês.</span><span class="sxs-lookup"><span data-stu-id="ba73b-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="ba73b-p105">Talvez você queira definir a chave primária para a nova tabela. Quando você cria a tabela, os campos na nova tabela herdam o tipo de dados e o tamanho do campo para cada campo nas tabelas subjacentes da consulta, mas nenhuma outra propriedade do campo ou da tabela é transferida.</span><span class="sxs-lookup"><span data-stu-id="ba73b-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="ba73b-127">Para adicionar dados a uma tabela existente, use a instrução [INSERT INTO](insert-into-statement-microsoft-access-sql.md) em vez de criar uma consulta acréscimo.</span><span class="sxs-lookup"><span data-stu-id="ba73b-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="ba73b-128">Para descobrir quais registros serão selecionados antes de executar a consulta criar tabela, primeiro examine os resultados de uma instrução [SELECT](select-statement-microsoft-access-sql.md) que usa os mesmos critérios de seleção.</span><span class="sxs-lookup"><span data-stu-id="ba73b-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="ba73b-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ba73b-129">Example</span></span>

<span data-ttu-id="ba73b-130">Este exemplo seleciona todos os registros na tabela Funcionários e copia-os para uma nova tabela chamada Emp Backup.</span><span class="sxs-lookup"><span data-stu-id="ba73b-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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

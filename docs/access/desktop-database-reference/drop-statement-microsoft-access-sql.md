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
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="cd709-102">Instrução DROP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="cd709-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="cd709-103">**Aplica-se ao**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd709-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd709-104">Exclui uma tabela, procedimento ou modo de exibição existente de um banco de dados ou exclui um índice existente de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="cd709-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="cd709-p101">O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de DROP nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access. Use os métodos **Delete** do ADO no lugar.</span><span class="sxs-lookup"><span data-stu-id="cd709-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd709-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd709-107">Syntax</span></span>

<span data-ttu-id="cd709-108">DROP {TABLE *tabela* | INDEX *índice* ON *tabela* | PROCEDURE *procedimento* | VIEW *exibição*}</span><span class="sxs-lookup"><span data-stu-id="cd709-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="cd709-109">A instrução DROP tem as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="cd709-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd709-110">Sair</span><span class="sxs-lookup"><span data-stu-id="cd709-110">Part</span></span></p></th>
<th><p><span data-ttu-id="cd709-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd709-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd709-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="cd709-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="cd709-113">O nome da tabela a ser excluída ou tabela da qual um índice será excluído.</span><span class="sxs-lookup"><span data-stu-id="cd709-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd709-114"><em>procedimento</em></span><span class="sxs-lookup"><span data-stu-id="cd709-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="cd709-115">O nome do procedimento a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cd709-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd709-116"><em>exibição</em></span><span class="sxs-lookup"><span data-stu-id="cd709-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="cd709-117">O nome do modo de exibição a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cd709-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd709-118"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="cd709-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="cd709-119">O nome do índice a ser excluído da tabela <em>.</em></span><span class="sxs-lookup"><span data-stu-id="cd709-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cd709-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd709-120">Remarks</span></span>

<span data-ttu-id="cd709-121">Você deve fechar a tabela antes de excluir ou remover um índice dela.</span><span class="sxs-lookup"><span data-stu-id="cd709-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="cd709-122">Você também pode usar [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para excluir um índice de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="cd709-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="cd709-p102">Você pode usar [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar uma tabela e [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ou ALTER TABLE para criar um índice. Para modificar uma tabela, use ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="cd709-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="cd709-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="cd709-125">Example</span></span>

<span data-ttu-id="cd709-126">O exemplo a seguir considera a existência de um índice NewIndex hipotético na tabela Funcionários no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="cd709-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="cd709-127">Este exemplo exclui o índice MyIndex na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="cd709-127">This example deletes the index MyIndex from the Employees table.</span></span>

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

<span data-ttu-id="cd709-128">Este exemplo exclui a tabela Funcionários do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd709-128">This example deletes the Employees table from the database.</span></span>

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

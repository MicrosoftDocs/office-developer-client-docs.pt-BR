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
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="ba11e-102">Instrução DROP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ba11e-102">DROP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ba11e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba11e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ba11e-104">Exclui uma tabela, um procedimento ou uma exibição existente de um banco de dados ou exclui um índice existente de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ba11e-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="ba11e-p101">[!OBSERVAçãO] O mecanismo de banco de dados do Microsoft Access não oferece suporte ao uso de DROP nem de nenhuma instrução DDL, com os bancos de dados cujos mecanismos sejam diferentes do Microsoft Access. Use os métodos **Delete** do ADO no lugar.</span><span class="sxs-lookup"><span data-stu-id="ba11e-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba11e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba11e-107">Syntax</span></span>

<span data-ttu-id="ba11e-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span><span class="sxs-lookup"><span data-stu-id="ba11e-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="ba11e-109">A instrução DROP tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="ba11e-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba11e-110">Parte</span><span class="sxs-lookup"><span data-stu-id="ba11e-110">Part</span></span></p></th>
<th><p><span data-ttu-id="ba11e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba11e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba11e-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="ba11e-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="ba11e-113">O nome da tabela a ser excluída ou a tabela da qual um índice deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ba11e-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba11e-114"><em>procedure</em></span><span class="sxs-lookup"><span data-stu-id="ba11e-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="ba11e-115">O nome do procedimento a ser criado.</span><span class="sxs-lookup"><span data-stu-id="ba11e-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ba11e-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="ba11e-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="ba11e-117">O nome da exibição a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="ba11e-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba11e-118"><em>índice</em></span><span class="sxs-lookup"><span data-stu-id="ba11e-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="ba11e-119">O nome do índice a ser excluído da <em>tabela</em>.</span><span class="sxs-lookup"><span data-stu-id="ba11e-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ba11e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba11e-120">Remarks</span></span>

<span data-ttu-id="ba11e-121">Para poder remover um índice da tabela ou excluí-la, você deve antes fechá-la.</span><span class="sxs-lookup"><span data-stu-id="ba11e-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="ba11e-122">Você também pode usar [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) para excluir um índice de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ba11e-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="ba11e-p102">Você pode usar [CREATE TABLE](create-table-statement-microsoft-access-sql.md) para criar uma tabela e [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ou ALTER TABLE para criar um índice. Para modificar uma tabela, use ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="ba11e-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="ba11e-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ba11e-125">Example</span></span>

<span data-ttu-id="ba11e-126">O exemplo a seguir considera a existência de um índice NewIndex hipotético na tabela Funcionários no banco de dados Northwind.</span><span class="sxs-lookup"><span data-stu-id="ba11e-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="ba11e-127">Este exemplo exclui o índice MyIndex na tabela Funcionários.</span><span class="sxs-lookup"><span data-stu-id="ba11e-127">This example deletes the index MyIndex from the Employees table.</span></span>

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

<span data-ttu-id="ba11e-128">Este exemplo exclui a tabela Funcionários do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ba11e-128">This example deletes the Employees table from the database.</span></span>

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

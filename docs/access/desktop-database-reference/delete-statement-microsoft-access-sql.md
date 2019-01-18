---
title: Exclua a instrução (Microsoft Access SQL)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715617"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="0cad1-102">Exclua a instrução (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0cad1-102">DELETE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="0cad1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cad1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0cad1-104">Cria uma consulta de exclusão que remove os registros de uma ou mais tabelas listadas na cláusula [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) que atenda à cláusula [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="0cad1-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause that satisfy the [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cad1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cad1-105">Syntax</span></span>

<span data-ttu-id="0cad1-106">Excluir \[ *tabela*. \* \] Da *tabela* onde *critérios*</span><span class="sxs-lookup"><span data-stu-id="0cad1-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="0cad1-107">A instrução DELETE tem estas partes:</span><span class="sxs-lookup"><span data-stu-id="0cad1-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cad1-108">Parte</span><span class="sxs-lookup"><span data-stu-id="0cad1-108">Part</span></span></p></th>
<th><p><span data-ttu-id="0cad1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cad1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cad1-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="0cad1-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="0cad1-111">O nome opcional da tabela da qual os registros são excluídos.</span><span class="sxs-lookup"><span data-stu-id="0cad1-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cad1-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="0cad1-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="0cad1-113">O nome da tabela da qual os registros são excluídos.</span><span class="sxs-lookup"><span data-stu-id="0cad1-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cad1-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="0cad1-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="0cad1-115">Uma expressão que determina quais registros serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="0cad1-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0cad1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cad1-116">Remarks</span></span>

<span data-ttu-id="0cad1-117">DELETE é especialmente útil quando você desejar excluir muitos registros.</span><span class="sxs-lookup"><span data-stu-id="0cad1-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="0cad1-p101">Para eliminar uma tabela inteira do banco de dados, você pode usar o método **Execute** com uma instrução [DROP](drop-statement-microsoft-access-sql.md). Se você excluir a tabela, contudo, a estrutura será perdida. Do contrário, quando você usar DELETE, somente os dados serão excluídos; a estrutura da tabela e todas as propriedades da tabela, como os atributos e os índices de campos, permanecerão intactos.</span><span class="sxs-lookup"><span data-stu-id="0cad1-p101">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement. If you delete the table, however, the structure is lost. In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="0cad1-p102">Você pode usar DELETE para remover registros das tabelas que estão em uma relação um-para-muitos com outras tabelas. As operações de exclusão em cascata fazem com que os registros nas tabelas, que estão no lado muitos da relação, sejam excluídos quando o registro correspondente no lado um da relação for excluído na consulta. Por exemplo, na relação entre as tabelas Clientes e Pedidos, a tabela Clientes está no lado um e a tabela Pedidos está no lado muito da relação. A exclusão de Clientes resulta na exclusão dos registros correspondentes em Pedidos, se a opção de exclusão em cascata estiver especificada.</span><span class="sxs-lookup"><span data-stu-id="0cad1-p102">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables. Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query. For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship. Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="0cad1-p103">Uma consulta de exclusão exclui registros inteiros, não apenas dados em campos específicos. Se você quiser excluir valores em um campo específico, crie uma consulta de atualização que altere os valores para **Null**.</span><span class="sxs-lookup"><span data-stu-id="0cad1-p103">A delete query deletes entire records, not just data in specific fields. If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="0cad1-p104">Depois de remover registros utilizando uma consulta de exclusão, você não poderá desfazer a operação. Se você quiser saber quais registros foram excluídos, primeiro examine os resultados de uma consulta de seleção que use os mesmos critérios e, em seguida, execute a consulta de exclusão.</span><span class="sxs-lookup"><span data-stu-id="0cad1-p104">After you remove records using a delete query, you cannot undo the operation. If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="0cad1-p105">Sempre faça cópias de backup dos dados. Se você excluir registros erroneamente, será possível recuperá-los das cópias de backup.</span><span class="sxs-lookup"><span data-stu-id="0cad1-p105">Maintain backup copies of your data at all times. If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="0cad1-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0cad1-131">Example</span></span>

<span data-ttu-id="0cad1-p106">Este exemplo exclui todos os registros de funcionários cujo cargo é Trainee. Quando a cláusula FROM inclui apenas uma tabela, não é necessário listar o nome da tabela na instrução DELETE.

</span><span class="sxs-lookup"><span data-stu-id="0cad1-p106">This example deletes all records for employees whose title is Trainee. When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

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

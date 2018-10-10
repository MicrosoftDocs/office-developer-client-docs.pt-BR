---
title: Instrução UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE Statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3affce9346e9e322bc588ca1c3be24867a1469d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463192"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="fc1fc-102">Instrução UPDATE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fc1fc-102">UPDATE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="fc1fc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc1fc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fc1fc-104">Cria uma consulta de atualização que altera os valores nos campos em uma tabela especificada com base em critérios específicos.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1fc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc1fc-105">Syntax</span></span>

<span data-ttu-id="fc1fc-106">ATUALIZAÇÃO *tabela* SET *newvalue* onde *critérios*;</span><span class="sxs-lookup"><span data-stu-id="fc1fc-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="fc1fc-107">A instrução UPDATE contém estas partes:</span><span class="sxs-lookup"><span data-stu-id="fc1fc-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc1fc-108">Parte</span><span class="sxs-lookup"><span data-stu-id="fc1fc-108">Part</span></span></p></th>
<th><p><span data-ttu-id="fc1fc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc1fc-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc1fc-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="fc1fc-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="fc1fc-111">O nome da tabela que contém os dados que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc1fc-112"><em>newvalue</em></span><span class="sxs-lookup"><span data-stu-id="fc1fc-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="fc1fc-113">Uma expressão que determina o valor a ser inserido em um determinado campo nos registros atualizados.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc1fc-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="fc1fc-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="fc1fc-p101">Uma expressão que determina quais registros serão atualizados. Somente os registros que atendem à expressão são atualizados.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fc1fc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc1fc-117">Remarks</span></span>

<span data-ttu-id="fc1fc-118">UPDATE é especialmente útil quando você deseja alterar muitos registros ou quando os registros que deseja alterar estão em várias tabelas.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="fc1fc-p102">Você pode alterar vários campos ao mesmo tempo. O exemplo a seguir aumenta os valores Total de Pedidos em 10% e os valores Frete em 3% para transportadoras no Reino Unido:</span><span class="sxs-lookup"><span data-stu-id="fc1fc-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="fc1fc-p103">UPDATE não gerar um conjunto de resultados. Além disso, depois de atualizar registros utilizando uma consulta de atualização, você não poderá desfazer a operação. Se você quiser saber quais registros foram atualizados, primeiro examine os resultados de uma consulta de seleção que use os mesmos critérios e, em seguida, execute a consulta de atualização.</span><span class="sxs-lookup"><span data-stu-id="fc1fc-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span></P>
> <LI>
> <P><span data-ttu-id="fc1fc-p104">Sempre faça cópias de backup dos dados. Se você atualizar registros erroneamente, será possível recuperá-los das cópias de backup.
</span><span class="sxs-lookup"><span data-stu-id="fc1fc-p104">Maintain backup copies of your data at all times. If you update the wrong records, you can retrieve them from your backup copies.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="fc1fc-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="fc1fc-126">Example</span></span>

<span data-ttu-id="fc1fc-127">Este exemplo altera os valores no campo Gerente para 5 em todos os registros de funcionários que têm atualmente valores 2 em  Gerente.

</span><span class="sxs-lookup"><span data-stu-id="fc1fc-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```

---
title: Propriedade Recordset.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ced8fc78729924ce271aa0fe38d77d287a131f13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307529"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="87562-102">Propriedade Recordset.UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="87562-102">Recordset.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="87562-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87562-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="87562-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87562-104">Syntax</span></span>

<span data-ttu-id="87562-105">*expressão* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="87562-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="87562-106">*expression* Uma variável que representa um objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87562-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87562-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="87562-107">Remarks</span></span>

<span data-ttu-id="87562-108">Quando um modo de lote **[Update](recordset-update-method-dao.md)** for executado, o DAO e a biblioteca de cursores em lotes do cliente criarão uma série de instruções SQL UPDATE para fazer as alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="87562-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="87562-109">Uma cláusula SQL WHERE será criada para cada atualização com a finalidade de isolar os registros marcados como alterados pela propriedade **[RecordStatus](recordset-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="87562-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="87562-110">Como alguns servidores remotos usam gatilhos ou outras formas para forçar a integridade referencial, é importante limitar, com frequência, os campos que estão sendo atualizados para apenas aqueles afetados pela alteração.</span><span class="sxs-lookup"><span data-stu-id="87562-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="87562-111">Para fazer isso, defina a propriedade **UpdateOptions** como uma das constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="87562-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="87562-112">Dessa forma, será executada somente a quantidade mínima absoluta de um código do gatilho.</span><span class="sxs-lookup"><span data-stu-id="87562-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="87562-113">Como resultado, a operação de atualização será executada de forma mais rápida e com menos erros potenciais.</span><span class="sxs-lookup"><span data-stu-id="87562-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="87562-p103">Você também pode concatenar qualquer uma das constantes **dbCriteriaDeleteInsert** ou **dbCriteriaUpdate** para determinar se será necessário usar um conjunto de instruções SQL DELETE e INSERT ou uma instrução SQL UPDATE para cada atualização durante o envio das modificações em lotes de volta para o servidor. No caso anterior, foram necessárias duas operações separadas para atualizar o registro. Em alguns casos, especialmente naqueles em que o sistema remoto implementou os gatilhos DELETE, INSERT e UPDATE, a escolha da definição da propriedade **UpdateOptions** correta pode impactar, de forma significativa, o desempenho.</span><span class="sxs-lookup"><span data-stu-id="87562-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="87562-117">Se você não especificar nenhuma constante, serão usadas **dbCriteriaUpdate** e **dbCriteriaKey**.</span><span class="sxs-lookup"><span data-stu-id="87562-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="87562-118">Os registros recentemente adicionados sempre gerarão instruções INSERT e os registros excluídos sempre gerarão instruções DELETE, de modo que essa propriedade se aplicará somente na forma como a bibiloteca de cursores atualizará os registros modificados.</span><span class="sxs-lookup"><span data-stu-id="87562-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="87562-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="87562-119">Example</span></span>

<span data-ttu-id="87562-120">Este exemplo usa as propriedades **BatchSize** e **UpdateOptions** para controlar os aspectos de qualquer atualização em lotes de um objeto **Recordset** específico.</span><span class="sxs-lookup"><span data-stu-id="87562-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```


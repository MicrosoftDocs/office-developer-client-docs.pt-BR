---
title: Propriedade Recordset2.UpdateOptions (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 2692480e-c472-dd8e-f91a-939776822ece
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191899(v=office.15)
ms:contentKeyID: 48543816
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d655ba231466ac41902dba3a1422ca02893938f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698663"
---
# <a name="recordset2updateoptions-property-dao"></a><span data-ttu-id="73583-102">Propriedade Recordset2.UpdateOptions (DAO)</span><span class="sxs-lookup"><span data-stu-id="73583-102">Recordset2.UpdateOptions property (DAO)</span></span>


<span data-ttu-id="73583-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="73583-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="73583-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73583-104">Syntax</span></span>

<span data-ttu-id="73583-105">*expressão* . UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="73583-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="73583-106">*expressão* Uma variável que representa um objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="73583-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73583-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="73583-107">Remarks</span></span>

<span data-ttu-id="73583-108">Quando um modo de lote **[Update](recordset2-update-method-dao.md)** for executado, o DAO e a biblioteca de cursores em lotes do cliente criarão uma série de instruções SQL UPDATE para fazer as alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="73583-108">When a batch-mode **[Update](recordset2-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="73583-109">Uma cláusula SQL WHERE será criada para cada atualização com a finalidade de isolar os registros marcados como alterados pela propriedade **[RecordStatus](recordset2-recordstatus-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="73583-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset2-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="73583-110">Como alguns servidores remotos usam gatilhos ou outras formas para forçar a integridade referencial, é importante limitar, com frequência, os campos que estão sendo atualizados para apenas aqueles afetados pela alteração.</span><span class="sxs-lookup"><span data-stu-id="73583-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="73583-111">Para fazer isso, defina a propriedade **UpdateOptions** como uma das constantes **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols** ou **dbCriteriaTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="73583-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="73583-112">Dessa forma, será executada somente a quantidade mínima absoluta de um código do gatilho.</span><span class="sxs-lookup"><span data-stu-id="73583-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="73583-113">Como resultado, a operação de atualização será executada de forma mais rápida e com menos erros potenciais.</span><span class="sxs-lookup"><span data-stu-id="73583-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="73583-p103">Você também pode concatenar qualquer uma das constantes **dbCriteriaDeleteInsert** ou **dbCriteriaUpdate** para determinar se será necessário usar um conjunto de instruções SQL DELETE e INSERT ou uma instrução SQL UPDATE para cada atualização durante o envio das modificações em lotes de volta para o servidor. No caso anterior, foram necessárias duas operações separadas para atualizar o registro. Em alguns casos, especialmente naqueles em que o sistema remoto implementou os gatilhos DELETE, INSERT e UPDATE, a escolha da definição da propriedade **UpdateOptions** correta pode impactar, de forma significativa, o desempenho.</span><span class="sxs-lookup"><span data-stu-id="73583-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="73583-117">Se você não especificar nenhuma constante, serão usadas **dbCriteriaUpdate** e **dbCriteriaKey**.</span><span class="sxs-lookup"><span data-stu-id="73583-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="73583-118">Os registros recentemente adicionados sempre gerarão instruções INSERT e os registros excluídos sempre gerarão instruções DELETE, de modo que essa propriedade se aplicará somente na forma como a bibiloteca de cursores atualizará os registros modificados.</span><span class="sxs-lookup"><span data-stu-id="73583-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>


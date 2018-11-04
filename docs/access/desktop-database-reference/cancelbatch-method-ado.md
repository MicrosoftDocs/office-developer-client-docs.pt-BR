---
title: Método CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88bf83cad220056d9ee21f300e5543030e5d18cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950073"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="46fd5-102">Método CancelBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="46fd5-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="46fd5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="46fd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46fd5-104">Cancela uma atualização em lotes pendente.</span><span class="sxs-lookup"><span data-stu-id="46fd5-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46fd5-105">Syntax</span></span>

<span data-ttu-id="46fd5-106">*conjunto de registros*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="46fd5-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="46fd5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46fd5-107">Parameters</span></span>

|<span data-ttu-id="46fd5-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="46fd5-108">Parameter</span></span>|<span data-ttu-id="46fd5-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="46fd5-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="46fd5-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="46fd5-110">*AffectRecords*</span></span> |<span data-ttu-id="46fd5-p101">Opcional. Um valor [AffectEnum](affectenum.md) que determina a quantidade de registros que serão afetados pelo método **CancelBatch**.</span><span class="sxs-lookup"><span data-stu-id="46fd5-p101">Optional. An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="46fd5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46fd5-113">Remarks</span></span>

<span data-ttu-id="46fd5-p102">Use o método **CancelBatch** para cancelar todas as atualizações pendentes em um [Recordset](recordset-object-ado.md) no modo de atualização em lotes. Se **Recordset** estiver no modo de atualização imediata, um erro será gerado se **CancelBatch** for chamado sem **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="46fd5-p102">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode. If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="46fd5-p103">Se você estiver editando o registro atual ou adicionando um novo registro ao chamar **CancelBatch**, o ADO chamará primeiro o método [CancelUpdate](cancelupdate-method-ado.md) para cancelar todas as alterações armazenadas em cache. Em seguida, todas as alterações pendentes serão canceladas no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="46fd5-p103">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes. After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="46fd5-p104">É possível que o registro atual não possa ser determinado após uma chamada de **CancelBatch**, principalmente se você estiver no processo de adição de um novo registro. Por esse motivo, convém definir a posição do registro atual para um local conhecido no **Recordset** após a chamada de **CancelBatch**. Por exemplo, chame o método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="46fd5-p104">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record. For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call. For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="46fd5-p105">Se a tentativa de cancelar as atualizações pendentes falhar devido a um conflito com os dados subjacentes (por exemplo, por causa da exclusão de um registro por outro usuário), o provedor retornará avisos à coleção [Errors](errors-collection-ado.md), mas não interromperá a execução do programa. Um erro em tempo de execução somente ocorrerá em caso de conflito em todos os registros solicitados. Use a propriedade [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.</span><span class="sxs-lookup"><span data-stu-id="46fd5-p105">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>


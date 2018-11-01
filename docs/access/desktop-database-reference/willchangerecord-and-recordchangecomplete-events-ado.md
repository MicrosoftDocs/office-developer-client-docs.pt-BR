---
title: Eventos WillChangeRecord e RecordChangeComplete (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete Events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 895a80cf4810088b5f18f4a9416e7eadc54a004f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878126"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a><span data-ttu-id="d3792-102">Eventos WillChangeRecord e RecordChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3792-102">WillChangeRecord and RecordChangeComplete Events (ADO)</span></span>


<span data-ttu-id="d3792-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3792-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d3792-p101">O evento **WillChangeRecord** é chamado antes da alteração de um ou mais registros (linhas) no [Recordset](recordset-object-ado.md). O evento **RecordChangeComplete** é chamado depois da alteração de um ou mais registros.</span><span class="sxs-lookup"><span data-stu-id="d3792-p101">The **WillChangeRecord** event is called before one or more records (rows) in the [Recordset](recordset-object-ado.md) change. The **RecordChangeComplete** event is called after one or more records change.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3792-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3792-106">Syntax</span></span>

<span data-ttu-id="d3792-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="d3792-107">WillChangeRecord*adReason*, *cRecords*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="d3792-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="d3792-108">RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="d3792-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3792-109">Parameters</span></span>

  - <span data-ttu-id="d3792-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="d3792-110">*adReason*</span></span>

  - <span data-ttu-id="d3792-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** ou **adRsnFirstChange**.</span><span class="sxs-lookup"><span data-stu-id="d3792-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, or **adRsnFirstChange**.</span></span>

  - <span data-ttu-id="d3792-113">*cRecords*</span><span class="sxs-lookup"><span data-stu-id="d3792-113">*cRecords*</span></span>

  - <span data-ttu-id="d3792-114">Um valor **Long** que indica o número de registros que foram alterados (afetados).</span><span class="sxs-lookup"><span data-stu-id="d3792-114">A **Long** value that indicates the number of records changing (affected).</span></span>

  - <span data-ttu-id="d3792-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="d3792-115">*pError*</span></span>

  - <span data-ttu-id="d3792-p103">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="d3792-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="d3792-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d3792-118">*adStatus*</span></span>

  - [<span data-ttu-id="d3792-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="d3792-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="d3792-p104">Quando **WillChangeRecord** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="d3792-p104">When **WillChangeRecord** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="d3792-122">Quando **RecordChangeComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="d3792-122">When **RecordChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="d3792-123">Antes do retorno de **WillChangeRecord**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação que gerou esse evento, ou como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d3792-123">Before **WillChangeRecord** returns, set this parameter to **adStatusCancel** to request cancellation of the operation that caused this event or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="d3792-124">Antes do retorno de **RecordChangeComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d3792-124">Before **RecordChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="d3792-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="d3792-125">*pRecordset*</span></span>

  - <span data-ttu-id="d3792-p105">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d3792-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3792-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3792-128">Remarks</span></span>

<span data-ttu-id="d3792-129">Um evento **WillChangeRecord** ou **RecordChangeComplete** pode ocorrer para o campo alterado em uma linha devido às seguintes operações de **Recordset**: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) e [CancelBatch](cancelbatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d3792-129">A **WillChangeRecord** or **RecordChangeComplete** event may occur for the first changed field in a row due to the following **Recordset** operations: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [CancelBatch](cancelbatch-method-ado.md).</span></span> <span data-ttu-id="d3792-130">O valor do **Recordset** [CursorType](cursortype-property-ado.md) determina quais operações causam os eventos ocorra.</span><span class="sxs-lookup"><span data-stu-id="d3792-130">The value of the **Recordset** [CursorType](cursortype-property-ado.md) determines which operations cause the events to occur.</span></span>

<span data-ttu-id="d3792-131">Durante o evento **WillChangeRecord** , a propriedade de [filtro](filter-property-ado.md) de **conjunto de registros** é definida como **adFilterAffectedRecords**.</span><span class="sxs-lookup"><span data-stu-id="d3792-131">During the **WillChangeRecord** event, the **Recordset** [Filter](filter-property-ado.md) property is set to **adFilterAffectedRecords**.</span></span> <span data-ttu-id="d3792-132">Você não poderá alterar essa propriedade enquanto estiver processando o evento.</span><span class="sxs-lookup"><span data-stu-id="d3792-132">You cannot change this property while processing the event.</span></span>

<span data-ttu-id="d3792-133">Você deve definir o parâmetro adStatus como adStatusUnwantedEvent para cada valor adReason possível, a fim de interromper totalmente as notificações de qualquer evento que inclua o parâmetro adReason.</span><span class="sxs-lookup"><span data-stu-id="d3792-133">You must set the adStatus parameter to adStatusUnwantedEvent for each possible adReason value in order to completely stop event noticiation for any event that includes an adReason parameter.</span></span>


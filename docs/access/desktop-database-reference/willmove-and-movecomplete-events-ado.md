---
title: Eventos WillMove e MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705957"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="7b98c-102">Eventos WillMove e MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="7b98c-102">WillMove and MoveComplete events (ADO)</span></span>

<span data-ttu-id="7b98c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b98c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b98c-p101">O evento **WillMove** é chamado antes que a operação pendente altere a sua posição atual no [Recordset](recordset-object-ado.md). O evento **MoveComplete** é chamado depois da alteração da posição atual no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7b98c-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b98c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b98c-106">Syntax</span></span>

<span data-ttu-id="7b98c-107">WillMove*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7b98c-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="7b98c-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7b98c-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="7b98c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b98c-109">Parameters</span></span>

|<span data-ttu-id="7b98c-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b98c-110">Parameter</span></span>|<span data-ttu-id="7b98c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b98c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7b98c-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="7b98c-112">*adReason*</span></span> |<span data-ttu-id="7b98c-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** ou **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="7b98c-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>|
|<span data-ttu-id="7b98c-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="7b98c-115">*pError*</span></span> |<span data-ttu-id="7b98c-p103">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="7b98c-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="7b98c-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="7b98c-118">*adStatus*</span></span> |<span data-ttu-id="7b98c-119">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="7b98c-119">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="7b98c-120">Quando **WillMove** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7b98c-120">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="7b98c-121">Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="7b98c-121">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="7b98c-122">Quando **MoveComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="7b98c-122">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span> <br/><br/><span data-ttu-id="7b98c-123">Antes do retorno de **WillMove**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação pendente, ou como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7b98c-123">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span> <br/><br/><span data-ttu-id="7b98c-124">Antes do retorno de **MoveComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="7b98c-124">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="7b98c-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="7b98c-125">*pRecordset*</span></span> |<span data-ttu-id="7b98c-p105">Um objeto [Recordset](recordset-object-ado.md). O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7b98c-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7b98c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b98c-128">Remarks</span></span>

<span data-ttu-id="7b98c-129">Um evento **WillMove** ou **MoveComplete** pode ocorrer devido aos seguintes operações de **Recordset** :</span><span class="sxs-lookup"><span data-stu-id="7b98c-129">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations:</span></span>

- [<span data-ttu-id="7b98c-130">Open</span><span class="sxs-lookup"><span data-stu-id="7b98c-130">Open</span></span>](open-method-ado-recordset.md)
- [<span data-ttu-id="7b98c-131">Move</span><span class="sxs-lookup"><span data-stu-id="7b98c-131">Move</span></span>](move-method-ado.md)
- [<span data-ttu-id="7b98c-132">Métodos MoveFirst</span><span class="sxs-lookup"><span data-stu-id="7b98c-132">MoveFirst</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="7b98c-133">MoveLast</span><span class="sxs-lookup"><span data-stu-id="7b98c-133">MoveLast</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="7b98c-134">MoveNext</span><span class="sxs-lookup"><span data-stu-id="7b98c-134">MoveNext</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [<span data-ttu-id="7b98c-135">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="7b98c-135">MovePrevious</span></span>](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [<span data-ttu-id="7b98c-136">AddNew</span><span class="sxs-lookup"><span data-stu-id="7b98c-136">AddNew</span></span>](addnew-method-ado.md)
- [<span data-ttu-id="7b98c-137">Requery</span><span class="sxs-lookup"><span data-stu-id="7b98c-137">Requery</span></span>](requery-method-ado.md)

<span data-ttu-id="7b98c-138">Esses eventos podem ocorrer devido às seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="7b98c-138">These events may occur because of the following properties:</span></span>

- [<span data-ttu-id="7b98c-139">Filtro</span><span class="sxs-lookup"><span data-stu-id="7b98c-139">Filter</span></span>](filter-property-ado.md)
- [<span data-ttu-id="7b98c-140">Índice</span><span class="sxs-lookup"><span data-stu-id="7b98c-140">Index</span></span>](index-property-ado.md)
- [<span data-ttu-id="7b98c-141">Bookmark</span><span class="sxs-lookup"><span data-stu-id="7b98c-141">Bookmark</span></span>](bookmark-property-ado.md)
- [<span data-ttu-id="7b98c-142">AbsolutePage</span><span class="sxs-lookup"><span data-stu-id="7b98c-142">AbsolutePage</span></span>](absolutepage-property-ado.md)
- [<span data-ttu-id="7b98c-143">AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="7b98c-143">AbsolutePosition</span></span>](absoluteposition-property-ado.md)

<span data-ttu-id="7b98c-144">Esses eventos também ocorrerão se um **Recordset** filho tiver eventos **Recordset** conectados e se o **Recordset** pai for movido.</span><span class="sxs-lookup"><span data-stu-id="7b98c-144">These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="7b98c-145">Você deve definir o parâmetro *adStatus* como **adStatusUnwantedEvent** para cada valor *adReason* possível para parar completamente a notificação de evento para qualquer evento que inclua um parâmetro *adReason*.</span><span class="sxs-lookup"><span data-stu-id="7b98c-145">You must set the *adStatus* parameter to **adStatusUnwantedEvent** for each possible *adReason* value in order to completely stop event notification for any event that includes an *adReason* parameter.</span></span>


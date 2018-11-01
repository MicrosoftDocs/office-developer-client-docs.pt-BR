---
title: Eventos WillMove e MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete Events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3b1a0e119d857947b78eb6adcfc9a5b1ba87e055
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868830"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="98d4d-102">Eventos WillMove e MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="98d4d-102">WillMove and MoveComplete Events (ADO)</span></span>


<span data-ttu-id="98d4d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="98d4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98d4d-p101">O evento **WillMove** é chamado antes que a operação pendente altere a sua posição atual no [Recordset](recordset-object-ado.md). O evento **MoveComplete** é chamado depois da alteração da posição atual no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d4d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98d4d-106">Syntax</span></span>

<span data-ttu-id="98d4d-107">WillMove*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="98d4d-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="98d4d-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="98d4d-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="98d4d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98d4d-109">Parameters</span></span>

  - <span data-ttu-id="98d4d-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="98d4d-110">*adReason*</span></span>

  - <span data-ttu-id="98d4d-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** ou **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="98d4d-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="98d4d-113">*pError*</span></span>

  - <span data-ttu-id="98d4d-p103">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="98d4d-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="98d4d-116">*adStatus*</span></span>

  - [<span data-ttu-id="98d4d-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="98d4d-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="98d4d-p104">Quando **WillMove** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="98d4d-120">Quando **MoveComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="98d4d-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="98d4d-121">Antes do retorno de **WillMove**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação pendente, ou como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="98d4d-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="98d4d-122">Antes do retorno de **MoveComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="98d4d-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="98d4d-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="98d4d-123">*pRecordset*</span></span>

  - <span data-ttu-id="98d4d-p105">Um objeto [Recordset](recordset-object-ado.md). O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d4d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="98d4d-126">Remarks</span></span>

<span data-ttu-id="98d4d-p106">Um evento **WillMove** ou **MoveComplete** pode ocorrer devido às seguintes operações de **Recordset**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) e [Requery](requery-method-ado.md). Esses eventos podem ocorrer devido às seguintes propriedades: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) e [AbsolutePosition](absoluteposition-property-ado.md). Esses eventos também ocorrerão se um **Recordset** filho tiver eventos **Recordset** conectados e se o **Recordset** pai for movido.</span><span class="sxs-lookup"><span data-stu-id="98d4d-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="98d4d-130">Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor adReason possível, a fim de interromper totalmente as notificações de qualquer evento que inclua o parâmetro adReason.</span><span class="sxs-lookup"><span data-stu-id="98d4d-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>


---
title: Eventos WillMove e MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5388601f1ac88e281a6abc5cfe1e644bdeebef28
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923564"
---
# <a name="willmove-and-movecomplete-events-ado"></a><span data-ttu-id="1c455-102">Eventos WillMove e MoveComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="1c455-102">WillMove and MoveComplete events (ADO)</span></span>


<span data-ttu-id="1c455-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c455-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c455-p101">O evento **WillMove** é chamado antes que a operação pendente altere a sua posição atual no [Recordset](recordset-object-ado.md). O evento **MoveComplete** é chamado depois da alteração da posição atual no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="1c455-p101">The **WillMove** event is called before a pending operation changes the current position in the [Recordset](recordset-object-ado.md). The **MoveComplete** event is called after the current position in the **Recordset** changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c455-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c455-106">Syntax</span></span>

<span data-ttu-id="1c455-107">WillMove*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1c455-107">WillMove*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="1c455-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1c455-108">MoveComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="1c455-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c455-109">Parameters</span></span>

  - <span data-ttu-id="1c455-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="1c455-110">*adReason*</span></span>

  - <span data-ttu-id="1c455-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** ou **adRsnRequery**.</span><span class="sxs-lookup"><span data-stu-id="1c455-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove**, or **adRsnRequery**.</span></span>

  - <span data-ttu-id="1c455-113">*pError*</span><span class="sxs-lookup"><span data-stu-id="1c455-113">*pError*</span></span>

  - <span data-ttu-id="1c455-p103">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="1c455-p103">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="1c455-116">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="1c455-116">*adStatus*</span></span>

  - [<span data-ttu-id="1c455-117">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="1c455-117">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="1c455-p104">Quando **WillMove** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="1c455-p104">When **WillMove** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="1c455-120">Quando **MoveComplete** é chamado, esse parâmetro é definido como **adStatusOK** se a operação que gerou o evento foi bem-sucedida, ou como **adStatusErrorsOccurred** se a operação falhar.</span><span class="sxs-lookup"><span data-stu-id="1c455-120">When **MoveComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="1c455-121">Antes do retorno de **WillMove**, defina esse parâmetro como **adStatusCancel**, para solicitar o cancelamento da operação pendente, ou como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1c455-121">Before **WillMove** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notications.</span></span>
    
    <span data-ttu-id="1c455-122">Antes do retorno de **MoveComplete**, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1c455-122">Before **MoveComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="1c455-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="1c455-123">*pRecordset*</span></span>

  - <span data-ttu-id="1c455-p105">Um objeto [Recordset](recordset-object-ado.md). O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="1c455-p105">A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c455-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c455-126">Remarks</span></span>

<span data-ttu-id="1c455-p106">Um evento **WillMove** ou **MoveComplete** pode ocorrer devido às seguintes operações de **Recordset**: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md) e [Requery](requery-method-ado.md). Esses eventos podem ocorrer devido às seguintes propriedades: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md) e [AbsolutePosition](absoluteposition-property-ado.md). Esses eventos também ocorrerão se um **Recordset** filho tiver eventos **Recordset** conectados e se o **Recordset** pai for movido.</span><span class="sxs-lookup"><span data-stu-id="1c455-p106">A **WillMove** or **MoveComplete** event may occur due to the following **Recordset** operations: [Open](open-method-ado-recordset.md), [Move](move-method-ado.md), [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md), [AddNew](addnew-method-ado.md), and [Requery](requery-method-ado.md). These events may occur because of the following properties: [Filter](filter-property-ado.md), [Index](index-property-ado.md), [Bookmark](bookmark-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), and [AbsolutePosition](absoluteposition-property-ado.md). These events also occur if a child **Recordset** has **Recordset** events connected and the parent **Recordset** is moved.</span></span>

<span data-ttu-id="1c455-130">Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor adReason possível, a fim de interromper totalmente as notificações de qualquer evento que inclua o parâmetro adReason.</span><span class="sxs-lookup"><span data-stu-id="1c455-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible adReason value in order to completely stop event notification for any event that includes an adReason parameter.</span></span>


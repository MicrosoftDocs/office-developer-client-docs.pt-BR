---
title: Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete Events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f9126005d8f11f859a3f45cbfec08e6612b59ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462962"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="79e84-102">Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="79e84-102">WillChangeRecordset and RecordsetChangeComplete Events (ADO)</span></span>


<span data-ttu-id="79e84-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="79e84-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="79e84-p101">O evento **WillChangeRecordset** é cancelado antes que uma operação pendente altere [Recordset](recordset-object-ado.md). O evento **RecordsetChangeComplete** é chamado depois que o **Recordset** for chamado.</span><span class="sxs-lookup"><span data-stu-id="79e84-p101">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md). The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e84-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79e84-106">Syntax</span></span>

<span data-ttu-id="79e84-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="79e84-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="79e84-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="79e84-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="79e84-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79e84-109">Parameters</span></span>

  - <span data-ttu-id="79e84-110">*adReason*</span><span class="sxs-lookup"><span data-stu-id="79e84-110">*adReason*</span></span>

  - <span data-ttu-id="79e84-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span><span class="sxs-lookup"><span data-stu-id="79e84-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>

  - <span data-ttu-id="79e84-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="79e84-113">*adStatus*</span></span>

  - [<span data-ttu-id="79e84-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="79e84-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="79e84-p103">Quando **WillChangeRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida. Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="79e84-p103">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="79e84-117">Quando **RecordsetChangeComplete** for chamado, esse parâmetro será configurado como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida, **adStatusErrorsOccurred** se a operação tiver falhado ou **adStatusCancel** se a operação associada ao evento **WillChangeRecordset** anteriormente aceito tiver sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="79e84-117">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span>
    
    <span data-ttu-id="79e84-118">Antes que **WillChangeRecordset** seja retornado, defina esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente ou defina esse parâmetro como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="79e84-118">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span>
    
    <span data-ttu-id="79e84-119">Antes que **WillChangeRecordset** ou **RecordsetChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="79e84-119">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="79e84-120">*pError*</span><span class="sxs-lookup"><span data-stu-id="79e84-120">*pError*</span></span>

  - <span data-ttu-id="79e84-p104">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="79e84-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="79e84-123">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="79e84-123">*pRecordset*</span></span>

  - <span data-ttu-id="79e84-p105">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="79e84-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="79e84-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="79e84-126">Remarks</span></span>

<span data-ttu-id="79e84-127">Um **WillChangeRecordset** ou **RecordsetChangeComplete** evento pode ocorrer devido aos métodos **Recordset** [Requery](requery-method-ado.md) ou [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="79e84-127">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="79e84-p106">Se o provedor não suportar indicadores, ocorrerá uma notificação de evento **RecordsetChange** sempre que novas linhas forem obtidas junto ao provedor. A frequência desse evento depende da propriedade **RecordsetCacheSize**.</span><span class="sxs-lookup"><span data-stu-id="79e84-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="79e84-130">Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor **adReason** possível para parar completamente a notificação de evento para qualquer evento que inclua um parâmetro **adReason**.</span><span class="sxs-lookup"><span data-stu-id="79e84-130">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>


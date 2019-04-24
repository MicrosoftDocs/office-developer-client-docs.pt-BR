---
title: Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302818"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a><span data-ttu-id="c6c9d-102">Eventos WillChangeRecordset e RecordsetChangeComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="c6c9d-102">WillChangeRecordset and RecordsetChangeComplete events (ADO)</span></span>

<span data-ttu-id="c6c9d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6c9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6c9d-104">O evento **WillChangeRecordset** é cancelado antes que uma operação pendente altere [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6c9d-104">The **WillChangeRecordset** event is called before a pending operation changes the [Recordset](recordset-object-ado.md).</span></span> <span data-ttu-id="c6c9d-105">O evento **RecordsetChangeComplete** é chamado depois que o **Recordset** for chamado.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-105">The **RecordsetChangeComplete** event is called after the **Recordset** has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c9d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6c9d-106">Syntax</span></span>

<span data-ttu-id="c6c9d-107">WillChangeRecordset*adReason*, *adStatus*, \*\* precaboset</span><span class="sxs-lookup"><span data-stu-id="c6c9d-107">WillChangeRecordset*adReason*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="c6c9d-108">RecordsetChangeComplete*adReason*, *perror*, *adStatus*, \*\* precaboset</span><span class="sxs-lookup"><span data-stu-id="c6c9d-108">RecordsetChangeComplete*adReason*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="c6c9d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6c9d-109">Parameters</span></span>

|<span data-ttu-id="c6c9d-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6c9d-110">Parameter</span></span>|<span data-ttu-id="c6c9d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6c9d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c6c9d-112">*adReason*</span><span class="sxs-lookup"><span data-stu-id="c6c9d-112">*adReason*</span></span> |<span data-ttu-id="c6c9d-p102">Um valor [EventReasonEnum](eventreasonenum.md) que especifica a razão para esse evento. Seu valor pode ser **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-p102">An [EventReasonEnum](eventreasonenum.md) value that specifies the reason for this event. Its value can be **adRsnRequery**, **adRsnResynch**, **adRsnClose**, **adRsnOpen**.</span></span>|
|<span data-ttu-id="c6c9d-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="c6c9d-115">*adStatus*</span></span> |<span data-ttu-id="c6c9d-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="c6c9d-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="c6c9d-117">Quando **WillChangeRecordset** for chamado, esse parâmetro será definido como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-117">When **WillChangeRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="c6c9d-118">Ele será definido como **adStatusCantDeny** se esse evento não puder solicitar o cancelamento da operação pendente.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-118">It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span> <br/><br/><span data-ttu-id="c6c9d-119">Quando **RecordsetChangeComplete** for chamado, esse parâmetro será configurado como **adStatusOK** se a operação que provocou o evento tiver sido bem-sucedida, **adStatusErrorsOccurred** se a operação tiver falhado ou **adStatusCancel** se a operação associada ao evento **WillChangeRecordset** anteriormente aceito tiver sido cancelada.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-119">When **RecordsetChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, **adStatusErrorsOccurred** if the operation failed, or **adStatusCancel** if the operation associated with the previously accepted **WillChangeRecordset** event has been canceled.</span></span> <br/><br/><span data-ttu-id="c6c9d-120">Antes que **WillChangeRecordset** seja retornado, defina esse parâmetro como **adStatusCancel** para solicitar o cancelamento da operação pendente ou defina esse parâmetro como adStatusUnwantedEvent para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-120">Before **WillChangeRecordset** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation or set this parameter to adStatusUnwantedEvent to prevent subsequent notifications.</span></span> <br/><br/><span data-ttu-id="c6c9d-121">Antes que **WillChangeRecordset** ou **RecordsetChangeComplete** seja retornado, defina esse parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-121">Before **WillChangeRecordset** or **RecordsetChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="c6c9d-122">*pError*</span><span class="sxs-lookup"><span data-stu-id="c6c9d-122">*pError*</span></span> |<span data-ttu-id="c6c9d-p104">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-p104">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="c6c9d-125">*precaboset*</span><span class="sxs-lookup"><span data-stu-id="c6c9d-125">*pRecordset*</span></span> |<span data-ttu-id="c6c9d-p105">Um objeto **Recordset**. O **Recordset** para o qual esse evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-p105">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c6c9d-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6c9d-128">Remarks</span></span>

<span data-ttu-id="c6c9d-129">Um evento **WillChangeRecordset** ou **RecordsetChangeComplete** pode ocorrer devido aos métodos **Recordset** [](requery-method-ado.md) Requery ou [Open](open-method-ado-recordset.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c9d-129">A **WillChangeRecordset** or **RecordsetChangeComplete** event may occur due to the **Recordset** [Requery](requery-method-ado.md) or [Open](open-method-ado-recordset.md) methods.</span></span>

<span data-ttu-id="c6c9d-p106">Se o provedor não suportar indicadores, ocorrerá uma notificação de evento **RecordsetChange** sempre que novas linhas forem obtidas junto ao provedor. A frequência desse evento depende da propriedade **RecordsetCacheSize**.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-p106">If the provider does not support bookmarks, a **RecordsetChange** event notification occurs each time new rows are retrieved from the provider. The frequency of this event depends on the **RecordsetCacheSize** property.</span></span>

<span data-ttu-id="c6c9d-132">Você deve definir o parâmetro **adStatus** como **adStatusUnwantedEvent** para cada valor **adReason** possível para parar completamente a notificação de evento para qualquer evento que inclua um parâmetro **adReason**.</span><span class="sxs-lookup"><span data-stu-id="c6c9d-132">You must set the **adStatus** parameter to **adStatusUnwantedEvent** for each possible **adReason** value in order to completely stop event notification for any event that includes an **adReason** parameter.</span></span>


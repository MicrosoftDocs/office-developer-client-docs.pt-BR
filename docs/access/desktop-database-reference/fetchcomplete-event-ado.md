---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293186"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="ef80c-102">Evento FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="ef80c-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="ef80c-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef80c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef80c-104">O evento **FetchComplete** é chamado depois de todos os registros em uma operação assíncrona prolongada terem sido recuperados no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ef80c-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef80c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef80c-105">Syntax</span></span>

<span data-ttu-id="ef80c-106">FetchComplete *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="ef80c-106">FetchComplete *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="ef80c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef80c-107">Parameters</span></span>

|<span data-ttu-id="ef80c-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef80c-108">Parameter</span></span>|<span data-ttu-id="ef80c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef80c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ef80c-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="ef80c-110">*pError*</span></span> |<span data-ttu-id="ef80c-p101">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="ef80c-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="ef80c-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ef80c-113">*adStatus*</span></span> |<span data-ttu-id="ef80c-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="ef80c-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="ef80c-115">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ef80c-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="ef80c-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="ef80c-116">*pRecordset*</span></span> |<span data-ttu-id="ef80c-p103">Um objeto **Recordset**. O objeto para o qual os registros foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="ef80c-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ef80c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef80c-119">Remarks</span></span>

<span data-ttu-id="ef80c-120">Para usar **FetchComplete** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ef80c-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


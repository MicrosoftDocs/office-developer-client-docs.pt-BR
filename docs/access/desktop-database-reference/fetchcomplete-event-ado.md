---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4b72bb3e05b4ef05358a80faffaa0ee4ce08a80
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882396"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="f2265-102">Evento FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2265-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="f2265-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2265-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f2265-104">O evento **FetchComplete** é chamado depois de todos os registros em uma operação assíncrona prolongada terem sido recuperados no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f2265-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2265-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2265-105">Syntax</span></span>

<span data-ttu-id="f2265-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="f2265-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="f2265-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2265-107">Parameters</span></span>

  - <span data-ttu-id="f2265-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="f2265-108">*pError*</span></span>

  - <span data-ttu-id="f2265-p101">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="f2265-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="f2265-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="f2265-111">*adStatus*</span></span>

  - [<span data-ttu-id="f2265-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="f2265-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="f2265-113">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f2265-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="f2265-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="f2265-114">*pRecordset*</span></span>

  - <span data-ttu-id="f2265-p102">Um objeto **Recordset**. O objeto para o qual os registros foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="f2265-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2265-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2265-117">Remarks</span></span>

<span data-ttu-id="f2265-118">Para usar **FetchComplete** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f2265-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


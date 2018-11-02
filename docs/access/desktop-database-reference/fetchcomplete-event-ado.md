---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ae09ff9bfcd694214a63fb630de52260ea7ac31
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925223"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="80597-102">Evento FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="80597-102">FetchComplete event (ADO)</span></span>


<span data-ttu-id="80597-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="80597-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="80597-104">O evento **FetchComplete** é chamado depois de todos os registros em uma operação assíncrona prolongada terem sido recuperados no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="80597-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="80597-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80597-105">Syntax</span></span>

<span data-ttu-id="80597-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="80597-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="80597-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80597-107">Parameters</span></span>

  - <span data-ttu-id="80597-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="80597-108">*pError*</span></span>

  - <span data-ttu-id="80597-p101">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="80597-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="80597-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="80597-111">*adStatus*</span></span>

  - [<span data-ttu-id="80597-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="80597-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="80597-113">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="80597-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="80597-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="80597-114">*pRecordset*</span></span>

  - <span data-ttu-id="80597-p102">Um objeto **Recordset**. O objeto para o qual os registros foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="80597-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="80597-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="80597-117">Remarks</span></span>

<span data-ttu-id="80597-118">Para usar **FetchComplete** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="80597-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


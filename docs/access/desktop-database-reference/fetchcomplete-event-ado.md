---
title: Evento FetchComplete (ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464037"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="2132e-102">Evento FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="2132e-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="2132e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2132e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2132e-104">O evento **FetchComplete** é chamado depois de todos os registros em uma operação assíncrona prolongada terem sido recuperados no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2132e-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2132e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2132e-105">Syntax</span></span>

<span data-ttu-id="2132e-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2132e-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="2132e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2132e-107">Parameters</span></span>

  - <span data-ttu-id="2132e-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="2132e-108">*pError*</span></span>

  - <span data-ttu-id="2132e-p101">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de **adStatus** for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="2132e-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="2132e-111">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="2132e-111">*adStatus*</span></span>

  - [<span data-ttu-id="2132e-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="2132e-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="2132e-113">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="2132e-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="2132e-114">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="2132e-114">*pRecordset*</span></span>

  - <span data-ttu-id="2132e-p102">Um objeto **Recordset**. O objeto para o qual os registros foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="2132e-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="2132e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2132e-117">Remarks</span></span>

<span data-ttu-id="2132e-118">Para usar **FetchComplete** com o Microsoft Visual Basic, é necessário o Visual Basic 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2132e-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: O suporta a alteração da base dos compromissos em uma pasta de calendário.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410067"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="ff2a8-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="ff2a8-103">IOlkApptRebaser</span></span>

<span data-ttu-id="ff2a8-104">O suporta a alteração da base dos compromissos em uma pasta de calendário.</span><span class="sxs-lookup"><span data-stu-id="ff2a8-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff2a8-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ff2a8-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff2a8-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="ff2a8-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="ff2a8-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="ff2a8-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="ff2a8-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ff2a8-108">Header file:</span></span>  <br/> |<span data-ttu-id="ff2a8-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="ff2a8-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="ff2a8-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ff2a8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff2a8-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="ff2a8-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="ff2a8-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ff2a8-112">Called by:</span></span>  <br/> |<span data-ttu-id="ff2a8-113">Aplicativos clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="ff2a8-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="ff2a8-114">Exposto em:</span><span class="sxs-lookup"><span data-stu-id="ff2a8-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="ff2a8-115">Objeto rebasing do Outlook</span><span class="sxs-lookup"><span data-stu-id="ff2a8-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ff2a8-116">Vtable order</span><span class="sxs-lookup"><span data-stu-id="ff2a8-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff2a8-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="ff2a8-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="ff2a8-118">Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para localizar os compromissos que precisam de alteração de base.</span><span class="sxs-lookup"><span data-stu-id="ff2a8-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="ff2a8-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="ff2a8-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="ff2a8-120">Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="ff2a8-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="ff2a8-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="ff2a8-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="ff2a8-122">Inicia uma tarefa para a alteração da base de compromisso, dada uma lista de compromissos, geralmente Obtida de **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="ff2a8-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="ff2a8-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="ff2a8-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="ff2a8-124">Aguarda a alteração da base do compromisso para concluir e recupera os resultados.</span><span class="sxs-lookup"><span data-stu-id="ff2a8-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff2a8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff2a8-125">See also</span></span>

- [<span data-ttu-id="ff2a8-126">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="ff2a8-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


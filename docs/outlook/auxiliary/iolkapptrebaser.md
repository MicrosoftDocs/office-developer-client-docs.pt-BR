---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Suporta a alteração da Base de compromissos em uma pasta de calendário.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765984"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="097c6-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="097c6-103">IOlkApptRebaser</span></span>

<span data-ttu-id="097c6-104">Suporta a alteração da Base de compromissos em uma pasta de calendário.</span><span class="sxs-lookup"><span data-stu-id="097c6-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="097c6-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="097c6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="097c6-106">Herda de:</span><span class="sxs-lookup"><span data-stu-id="097c6-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="097c6-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="097c6-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="097c6-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="097c6-108">Header file:</span></span>  <br/> |<span data-ttu-id="097c6-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="097c6-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="097c6-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="097c6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="097c6-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="097c6-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="097c6-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="097c6-112">Called by:</span></span>  <br/> |<span data-ttu-id="097c6-113">Aplicativos de cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="097c6-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="097c6-114">Expostas no:</span><span class="sxs-lookup"><span data-stu-id="097c6-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="097c6-115">REBASE de objeto do Outlook</span><span class="sxs-lookup"><span data-stu-id="097c6-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="097c6-116">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="097c6-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="097c6-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="097c6-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="097c6-118">Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.</span><span class="sxs-lookup"><span data-stu-id="097c6-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="097c6-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="097c6-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="097c6-120">Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.</span><span class="sxs-lookup"><span data-stu-id="097c6-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="097c6-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="097c6-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="097c6-122">Inicia uma tarefa a alteração da compromisso base fornecida uma lista de compromissos, normalmente obtido da **EndEnumerateAppointments**.</span><span class="sxs-lookup"><span data-stu-id="097c6-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="097c6-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="097c6-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="097c6-124">Aguardará compromisso a alteração da base para concluir e recupera os resultados.</span><span class="sxs-lookup"><span data-stu-id="097c6-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="097c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="097c6-125">See also</span></span>

- [<span data-ttu-id="097c6-126">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="097c6-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


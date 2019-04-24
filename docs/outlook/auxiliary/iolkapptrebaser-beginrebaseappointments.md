---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Inicia uma tarefa para alterar a base de compromisso, dada uma lista de compromissos, geralmente obtida de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: f0f2377f30de7688aaa4196e3a046c664c2128aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321907"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="e277d-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="e277d-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="e277d-104">Inicia uma tarefa para alterar a base de compromisso, dada uma lista de compromissos, geralmente obtida de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e277d-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e277d-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e277d-105">Quick info</span></span>

<span data-ttu-id="e277d-106">Confira [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="e277d-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="e277d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e277d-107">Parameters</span></span>

<span data-ttu-id="e277d-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="e277d-108">_pRows_</span></span>
  
> <span data-ttu-id="e277d-109">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e277d-109">[in] Required.</span></span> <span data-ttu-id="e277d-110">Um ponteiro para uma estrutura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="e277d-110">A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing.</span></span> <span data-ttu-id="e277d-111">Essa estrutura é obtida em uma chamada anterior para [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e277d-111">This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="e277d-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="e277d-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="e277d-113">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="e277d-113">[in] Optional.</span></span> <span data-ttu-id="e277d-114">Um ponteiro para uma função de progresso da tarefa de alteração da base para receber progresso.</span><span class="sxs-lookup"><span data-stu-id="e277d-114">A pointer to a rebase task progress function to receive progress.</span></span> <span data-ttu-id="e277d-115">**PFNREBASETASKPROGRESS** é definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="e277d-115">**PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="e277d-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="e277d-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="e277d-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="e277d-117">[out] Optional.</span></span> <span data-ttu-id="e277d-118">Um ponteiro para uma função de conclusão de tarefa de alteração da base para receber notificação de conclusão de alteração da base.</span><span class="sxs-lookup"><span data-stu-id="e277d-118">A pointer to a rebase task completion function to receive notification of rebase completion.</span></span> <span data-ttu-id="e277d-119">**PFNREBASETASKCOMPLETE** é definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="e277d-119">**PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="e277d-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="e277d-120">_ppContext_</span></span>
  
> <span data-ttu-id="e277d-121">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="e277d-121">[out] Required.</span></span> <span data-ttu-id="e277d-122">Um ponteiro para um ponteiro para o contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="e277d-122">A pointer to a pointer to the returned context.</span></span> <span data-ttu-id="e277d-123">Essa estrutura geralmente é passada para [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="e277d-123">This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e277d-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e277d-124">Return values</span></span>

<span data-ttu-id="e277d-125">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e277d-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e277d-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e277d-126">Remarks</span></span>

<span data-ttu-id="e277d-127">Esta tarefa é executada em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="e277d-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e277d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e277d-128">See also</span></span>

- [<span data-ttu-id="e277d-129">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="e277d-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


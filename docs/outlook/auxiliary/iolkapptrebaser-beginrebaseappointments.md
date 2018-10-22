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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396089"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="8e1c6-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="8e1c6-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="8e1c6-104">Inicia uma tarefa para alterar a base de compromisso, dada uma lista de compromissos, geralmente obtida de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8e1c6-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8e1c6-105">Quick info</span></span>

<span data-ttu-id="8e1c6-106">Confira [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="8e1c6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e1c6-107">Parameters</span></span>

<span data-ttu-id="8e1c6-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="8e1c6-108">_pRows_</span></span>
  
> <span data-ttu-id="8e1c6-109">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-109">[in] Required.</span></span> <span data-ttu-id="8e1c6-110">Um ponteiro para uma estrutura [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam de alteração programática.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-110">A pointer to an [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing.</span></span> <span data-ttu-id="8e1c6-111">Essa estrutura é obtida em uma chamada anterior para [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-111">This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="8e1c6-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="8e1c6-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="8e1c6-113">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-113">[in] Optional.</span></span> <span data-ttu-id="8e1c6-114">Um ponteiro para uma função de progresso da tarefa de alteração da base para receber progresso.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-114">A pointer to a rebase task progress function to receive progress.</span></span> <span data-ttu-id="8e1c6-115">**PFNREBASETASKPROGRESS** é definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8e1c6-115">**PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="8e1c6-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="8e1c6-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="8e1c6-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-117">[out] Optional.</span></span> <span data-ttu-id="8e1c6-118">Um ponteiro para uma função de conclusão de tarefa de alteração da base para receber notificação de conclusão de alteração da base.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-118">A pointer to a rebase task completion function to receive notification of rebase completion.</span></span> <span data-ttu-id="8e1c6-119">**PFNREBASETASKCOMPLETE** é definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="8e1c6-119">**PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="8e1c6-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="8e1c6-120">_ppContext_</span></span>
  
> <span data-ttu-id="8e1c6-121">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-121">[out] Required.</span></span> <span data-ttu-id="8e1c6-122">Um ponteiro para um ponteiro para o contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-122">A pointer to a pointer to the returned context.</span></span> <span data-ttu-id="8e1c6-123">Essa estrutura geralmente é passada para [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="8e1c6-123">This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8e1c6-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8e1c6-124">Return Values</span></span>

<span data-ttu-id="8e1c6-125">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e1c6-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e1c6-126">Remarks</span></span>

<span data-ttu-id="8e1c6-127">Esta tarefa é executada em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="8e1c6-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e1c6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e1c6-128">See also</span></span>

- [<span data-ttu-id="8e1c6-129">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="8e1c6-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


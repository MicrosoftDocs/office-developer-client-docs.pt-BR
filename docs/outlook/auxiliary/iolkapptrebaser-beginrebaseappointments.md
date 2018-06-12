---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Inicia uma tarefa a alteração da base compromisso fornecida uma lista de compromissos, normalmente obtido da IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: 2becb305eebe448e2adecf91c2a111f86d97fe50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765996"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a><span data-ttu-id="a0a96-103">IOlkApptRebaser::BeginRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="a0a96-103">IOlkApptRebaser::BeginRebaseAppointments</span></span>

<span data-ttu-id="a0a96-104">Inicia uma tarefa a alteração da compromisso base fornecida uma lista de compromissos, normalmente obtido da [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="a0a96-104">Begins a task for appointment rebasing given a list of appointments, usually obtained from [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a0a96-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a0a96-105">Quick info</span></span>

<span data-ttu-id="a0a96-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="a0a96-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="a0a96-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a0a96-107">Parameters</span></span>

<span data-ttu-id="a0a96-108">_pRows_</span><span class="sxs-lookup"><span data-stu-id="a0a96-108">_pRows_</span></span>
  
> <span data-ttu-id="a0a96-109">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a0a96-109">[in] Required.</span></span> <span data-ttu-id="a0a96-110">Um ponteiro para uma estrutura de [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) que descreve os compromissos que precisam a alteração da base.</span><span class="sxs-lookup"><span data-stu-id="a0a96-110">A pointer to an [SRowSet](http://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) structure that describes the appointments that need rebasing.</span></span> <span data-ttu-id="a0a96-111">Essa estrutura é obtida geralmente uma chamada anterior ao [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="a0a96-111">This structure is usually obtained from a prior call to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
<span data-ttu-id="a0a96-112">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="a0a96-112">_pfnProgress_</span></span>
  
> <span data-ttu-id="a0a96-113">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0a96-113">[in] Optional.</span></span> <span data-ttu-id="a0a96-114">Um ponteiro para uma função de andamento de tarefa alterar para receber o progresso.</span><span class="sxs-lookup"><span data-stu-id="a0a96-114">A pointer to a rebase task progress function to receive progress.</span></span> <span data-ttu-id="a0a96-115">**PFNREBASETASKPROGRESS** é definido em tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="a0a96-115">**PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="a0a96-116">_pfnComplete_</span><span class="sxs-lookup"><span data-stu-id="a0a96-116">_pfnComplete_</span></span>
  
> <span data-ttu-id="a0a96-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a0a96-117">[out] Optional.</span></span> <span data-ttu-id="a0a96-118">Um ponteiro para uma função de conclusão de tarefa alterar para receber uma notificação de conclusão de alterar.</span><span class="sxs-lookup"><span data-stu-id="a0a96-118">A pointer to a rebase task completion function to receive notification of rebase completion.</span></span> <span data-ttu-id="a0a96-119">**PFNREBASETASKCOMPLETE** é definido em tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="a0a96-119">**PFNREBASETASKCOMPLETE** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="a0a96-120">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="a0a96-120">_ppContext_</span></span>
  
> <span data-ttu-id="a0a96-121">[out] Necessário.</span><span class="sxs-lookup"><span data-stu-id="a0a96-121">[out] Required.</span></span> <span data-ttu-id="a0a96-122">Um ponteiro para um ponteiro para o contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="a0a96-122">A pointer to a pointer to the returned context.</span></span> <span data-ttu-id="a0a96-123">Nesse contexto geralmente será transmitido ao [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="a0a96-123">This context will usually be passed to [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a0a96-124">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a0a96-124">Return values</span></span>

<span data-ttu-id="a0a96-125">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a0a96-125">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0a96-126">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="a0a96-126">Remarks</span></span>

<span data-ttu-id="a0a96-127">Esta tarefa é executada em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="a0a96-127">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0a96-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0a96-128">See also</span></span>

- [<span data-ttu-id="a0a96-129">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="a0a96-129">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


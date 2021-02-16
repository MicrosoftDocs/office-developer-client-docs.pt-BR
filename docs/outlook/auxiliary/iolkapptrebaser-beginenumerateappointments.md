---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam ser baseados.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407267"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="a49cd-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="a49cd-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="a49cd-104">Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam ser baseados.</span><span class="sxs-lookup"><span data-stu-id="a49cd-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a49cd-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a49cd-105">Quick info</span></span>

<span data-ttu-id="a49cd-106">Confira [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="a49cd-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="a49cd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a49cd-107">Parameters</span></span>

<span data-ttu-id="a49cd-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="a49cd-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="a49cd-109">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a49cd-109">[in] Optional.</span></span> <span data-ttu-id="a49cd-110">Um ponteiro para uma função de progresso da tarefa de alteração da base para receber progresso.</span><span class="sxs-lookup"><span data-stu-id="a49cd-110">A pointer to a rebase task progress function to receive progress.</span></span> <span data-ttu-id="a49cd-111">**PFNREBASETASKPROGRESS** é definido em tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="a49cd-111">**PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="a49cd-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="a49cd-112">_ppContext_</span></span>
  
> <span data-ttu-id="a49cd-113">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="a49cd-113">[out] Required.</span></span> <span data-ttu-id="a49cd-114">Um ponteiro para um ponteiro para o contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="a49cd-114">A pointer to a pointer to the returned context.</span></span> <span data-ttu-id="a49cd-115">Esse contexto será passado para [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="a49cd-115">This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a49cd-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a49cd-116">Return values</span></span>

<span data-ttu-id="a49cd-117">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a49cd-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a49cd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a49cd-118">Remarks</span></span>

<span data-ttu-id="a49cd-119">Esta tarefa é executada em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="a49cd-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a49cd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a49cd-120">See also</span></span>

- [<span data-ttu-id="a49cd-121">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="a49cd-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


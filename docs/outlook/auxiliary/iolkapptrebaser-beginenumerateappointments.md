---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.
ms.openlocfilehash: 2ad26692483d87166a538ec2f04d3fc13b9ea930
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765977"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a><span data-ttu-id="af360-103">IOlkApptRebaser::BeginEnumerateAppointments</span><span class="sxs-lookup"><span data-stu-id="af360-103">IOlkApptRebaser::BeginEnumerateAppointments</span></span>

<span data-ttu-id="af360-104">Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.</span><span class="sxs-lookup"><span data-stu-id="af360-104">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="af360-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="af360-105">Quick info</span></span>

<span data-ttu-id="af360-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="af360-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a><span data-ttu-id="af360-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af360-107">Parameters</span></span>

<span data-ttu-id="af360-108">_pfnProgress_</span><span class="sxs-lookup"><span data-stu-id="af360-108">_pfnProgress_</span></span>
  
> <span data-ttu-id="af360-109">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="af360-109">[in] Optional.</span></span> <span data-ttu-id="af360-110">Um ponteiro para uma função de andamento de tarefa alterar para receber o progresso.</span><span class="sxs-lookup"><span data-stu-id="af360-110">A pointer to a rebase task progress function to receive progress.</span></span> <span data-ttu-id="af360-111">**PFNREBASETASKPROGRESS** é definido em tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="af360-111">**PFNREBASETASKPROGRESS** is defined in tzmovelib.h.</span></span> 
    
<span data-ttu-id="af360-112">_ppContext_</span><span class="sxs-lookup"><span data-stu-id="af360-112">_ppContext_</span></span>
  
> <span data-ttu-id="af360-113">[out] Necessário.</span><span class="sxs-lookup"><span data-stu-id="af360-113">[out] Required.</span></span> <span data-ttu-id="af360-114">Um ponteiro para um ponteiro para o contexto retornado.</span><span class="sxs-lookup"><span data-stu-id="af360-114">A pointer to a pointer to the returned context.</span></span> <span data-ttu-id="af360-115">Nesse contexto será transmitido ao [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span><span class="sxs-lookup"><span data-stu-id="af360-115">This context will be passed to [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="af360-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="af360-116">Return values</span></span>

<span data-ttu-id="af360-117">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="af360-117">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af360-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="af360-118">Remarks</span></span>

<span data-ttu-id="af360-119">Esta tarefa é executada em um novo segmento.</span><span class="sxs-lookup"><span data-stu-id="af360-119">This task runs on a new thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af360-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="af360-120">See also</span></span>

- [<span data-ttu-id="af360-121">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="af360-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


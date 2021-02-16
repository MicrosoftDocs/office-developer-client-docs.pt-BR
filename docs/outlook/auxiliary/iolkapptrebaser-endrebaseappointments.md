---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Aguarda a conclusão da base de compromissos e recupera os resultados.
ms.openlocfilehash: a6e62cff9efea1fc7079d04bc9b032b5637f8847
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430998"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="88032-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="88032-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="88032-104">Aguarda a conclusão da base de compromissos e recupera os resultados.</span><span class="sxs-lookup"><span data-stu-id="88032-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="88032-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="88032-105">Quick info</span></span>

<span data-ttu-id="88032-106">Confira [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="88032-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="88032-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88032-107">Parameters</span></span>

<span data-ttu-id="88032-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="88032-108">_pContext_</span></span>
  
> <span data-ttu-id="88032-109">[in] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="88032-109">[in] Required.</span></span> <span data-ttu-id="88032-110">Um ponteiro para o contexto obtido de uma chamada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="88032-110">A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="88032-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="88032-111">_phResult_</span></span>
  
> <span data-ttu-id="88032-112">[out] Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="88032-112">[out] Required.</span></span> <span data-ttu-id="88032-113">Um ponteiro para um **HRESULT** para recuperar o resultado da operação de base.</span><span class="sxs-lookup"><span data-stu-id="88032-113">A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="88032-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="88032-114">Return values</span></span>

<span data-ttu-id="88032-115">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="88032-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88032-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="88032-116">See also</span></span>

- [<span data-ttu-id="88032-117">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="88032-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


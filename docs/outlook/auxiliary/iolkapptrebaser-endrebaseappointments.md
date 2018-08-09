---
title: IOlkApptRebaserEndRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e47d5a8d-6a13-f430-fbfd-00df04b4a006
description: Aguardará compromisso a alteração da base para concluir e recupera os resultados.
ms.openlocfilehash: fd27021ce05b1d5b95fd258e0ee89b5bd4f2c7db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765992"
---
# <a name="iolkapptrebaserendrebaseappointments"></a><span data-ttu-id="68513-103">IOlkApptRebaser::EndRebaseAppointments</span><span class="sxs-lookup"><span data-stu-id="68513-103">IOlkApptRebaser::EndRebaseAppointments</span></span>

<span data-ttu-id="68513-104">Aguardará compromisso a alteração da base para concluir e recupera os resultados.</span><span class="sxs-lookup"><span data-stu-id="68513-104">Waits for appointment rebasing to complete and retrieves the results.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="68513-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="68513-105">Quick info</span></span>

<span data-ttu-id="68513-106">Consulte [IOlkApptRebaser](iolkapptrebaser.md).</span><span class="sxs-lookup"><span data-stu-id="68513-106">See [IOlkApptRebaser](iolkapptrebaser.md).</span></span>
  
```cpp
HRESULT EndRebaseAppointments( 
    void *pContext, 
    HRESULT *phResult);
```

## <a name="parameters"></a><span data-ttu-id="68513-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68513-107">Parameters</span></span>

<span data-ttu-id="68513-108">_pContext_</span><span class="sxs-lookup"><span data-stu-id="68513-108">_pContext_</span></span>
  
> <span data-ttu-id="68513-109">[in] Necessário.</span><span class="sxs-lookup"><span data-stu-id="68513-109">[in] Required.</span></span> <span data-ttu-id="68513-110">Um ponteiro para o contexto obtido de uma chamada para [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="68513-110">A pointer to the context obtained from a call to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="68513-111">_phResult_</span><span class="sxs-lookup"><span data-stu-id="68513-111">_phResult_</span></span>
  
> <span data-ttu-id="68513-112">[out] Necessário.</span><span class="sxs-lookup"><span data-stu-id="68513-112">[out] Required.</span></span> <span data-ttu-id="68513-113">Um ponteiro para um **HRESULT** para recuperar o resultado da operação REBASE.</span><span class="sxs-lookup"><span data-stu-id="68513-113">A pointer to an **HRESULT** to retrieve the result of the rebasing operation.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="68513-114">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="68513-114">Return values</span></span>

<span data-ttu-id="68513-115">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="68513-115">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68513-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="68513-116">See also</span></span>

- [<span data-ttu-id="68513-117">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="68513-117">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


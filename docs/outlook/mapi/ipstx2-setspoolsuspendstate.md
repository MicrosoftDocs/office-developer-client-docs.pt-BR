---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b6a36c1e0c3854342b627b6fddd6eb5459211f62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590425"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="5b96b-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="5b96b-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="5b96b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b96b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b96b-105">Define o estado suspenso em spooler.</span><span class="sxs-lookup"><span data-stu-id="5b96b-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="5b96b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b96b-106">Parameters</span></span>

 <span data-ttu-id="5b96b-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="5b96b-107">_ulState_</span></span>
  
> <span data-ttu-id="5b96b-108">[in] O estado para definir o spooler.</span><span class="sxs-lookup"><span data-stu-id="5b96b-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="5b96b-109">Ele deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5b96b-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="5b96b-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="5b96b-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="5b96b-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="5b96b-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="5b96b-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b96b-112">See also</span></span>



[<span data-ttu-id="5b96b-113">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="5b96b-113">MAPI Constants</span></span>](mapi-constants.md)


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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 30ec82788e46ca07c6529ce74872e0a0c7c012a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767673"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="ee0e9-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="ee0e9-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="ee0e9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee0e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee0e9-105">Define o estado suspenso em spooler.</span><span class="sxs-lookup"><span data-stu-id="ee0e9-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="ee0e9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ee0e9-106">Parameters</span></span>

 <span data-ttu-id="ee0e9-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="ee0e9-107">_ulState_</span></span>
  
> <span data-ttu-id="ee0e9-108">[in] O estado para definir o spooler.</span><span class="sxs-lookup"><span data-stu-id="ee0e9-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="ee0e9-109">Ele deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ee0e9-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="ee0e9-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="ee0e9-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="ee0e9-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="ee0e9-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="ee0e9-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee0e9-112">See also</span></span>



[<span data-ttu-id="ee0e9-113">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ee0e9-113">MAPI Constants</span></span>](mapi-constants.md)


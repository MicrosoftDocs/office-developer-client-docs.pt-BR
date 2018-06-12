---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767111"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="5d691-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="5d691-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="5d691-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d691-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d691-105">Obtém o estado atual de online ou offline, de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="5d691-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="5d691-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5d691-106">Parameters</span></span>

 <span data-ttu-id="5d691-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="5d691-107">_pulState_</span></span>
  
> <span data-ttu-id="5d691-108">[out] O estado online ou offline atual de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="5d691-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="5d691-109">Ele deve ser um destes dois valores:</span><span class="sxs-lookup"><span data-stu-id="5d691-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="5d691-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5d691-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="5d691-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5d691-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="5d691-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d691-112">See also</span></span>



[<span data-ttu-id="5d691-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="5d691-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="5d691-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="5d691-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="5d691-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="5d691-115">MAPI Constants</span></span>](mapi-constants.md)


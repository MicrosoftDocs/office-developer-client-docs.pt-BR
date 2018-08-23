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
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568200"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="d9a79-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d9a79-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="d9a79-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9a79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9a79-105">Obtém o estado atual de online ou offline, de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="d9a79-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="d9a79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9a79-106">Parameters</span></span>

 <span data-ttu-id="d9a79-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="d9a79-107">_pulState_</span></span>
  
> <span data-ttu-id="d9a79-108">[out] O estado online ou offline atual de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="d9a79-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="d9a79-109">Ele deve ser um destes dois valores:</span><span class="sxs-lookup"><span data-stu-id="d9a79-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="d9a79-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="d9a79-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="d9a79-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="d9a79-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="d9a79-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9a79-112">See also</span></span>



[<span data-ttu-id="d9a79-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="d9a79-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="d9a79-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="d9a79-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="d9a79-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d9a79-115">MAPI Constants</span></span>](mapi-constants.md)


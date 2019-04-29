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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f5170ceb443dcde075440bf84d29000afe4680c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419867"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="be189-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="be189-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="be189-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be189-105">Obtém o estado online ou offline atual de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="be189-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="be189-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be189-106">Parameters</span></span>

 <span data-ttu-id="be189-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="be189-107">_pulState_</span></span>
  
> <span data-ttu-id="be189-108">bota O estado atual online ou offline de um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="be189-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="be189-109">Deve ser um destes dois valores:</span><span class="sxs-lookup"><span data-stu-id="be189-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="be189-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="be189-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="be189-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="be189-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="be189-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="be189-112">See also</span></span>



[<span data-ttu-id="be189-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="be189-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="be189-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="be189-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="be189-115">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="be189-115">MAPI Constants</span></span>](mapi-constants.md)


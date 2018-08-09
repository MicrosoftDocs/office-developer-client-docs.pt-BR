---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Este método foi preterido no OSC 1.1.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770853"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="762f0-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="762f0-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="762f0-104">Este método foi preterido no OSC 1.1.</span><span class="sxs-lookup"><span data-stu-id="762f0-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="762f0-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="762f0-105">Remarks</span></span>

<span data-ttu-id="762f0-106">Iniciando no OSC 1.1, o OSC chama não são mais **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="762f0-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="762f0-107">O OSC ignora o valor de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="762f0-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="762f0-108">Para dar suporte à pesquisa de atividades dinâmico, implemente o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="762f0-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="762f0-109">Defina **cacheActivities** como **Falso**e **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="762f0-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="762f0-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="762f0-110">See also</span></span>

- [<span data-ttu-id="762f0-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="762f0-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)


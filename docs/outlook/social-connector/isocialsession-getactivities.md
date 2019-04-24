---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Esse método foi preterido no OSC 1,1.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285452"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="51e3c-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="51e3c-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="51e3c-104">Esse método foi preterido no OSC 1,1.</span><span class="sxs-lookup"><span data-stu-id="51e3c-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="51e3c-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="51e3c-105">Remarks</span></span>

<span data-ttu-id="51e3c-106">A partir do OSC 1,1, o OSC não chama \*\*\*\* mais getactivities.</span><span class="sxs-lookup"><span data-stu-id="51e3c-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="51e3c-107">O OSC ignora o valor de **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="51e3c-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="51e3c-108">Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) .</span><span class="sxs-lookup"><span data-stu-id="51e3c-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="51e3c-109">Defina **cacheActivities** como **false**e **getactivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2:: GetActivitiesEx** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="51e3c-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51e3c-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="51e3c-110">See also</span></span>

- [<span data-ttu-id="51e3c-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51e3c-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)


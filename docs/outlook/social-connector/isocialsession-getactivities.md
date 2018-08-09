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
# <a name="isocialsessiongetactivities"></a>ISocialSession::GetActivities

Este método foi preterido no OSC 1.1.
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a>Comentários

Iniciando no OSC 1.1, o OSC chama não são mais **GetActivities**. O OSC ignora o valor de **dynamicActivitiesLookup**. Para dar suporte à pesquisa de atividades dinâmico, implemente o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Defina **cacheActivities** como **Falso**e **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso. 
  
## <a name="see-also"></a>Confira também

- [ISocialSession : IUnknown](isocialsessioniunknown.md)


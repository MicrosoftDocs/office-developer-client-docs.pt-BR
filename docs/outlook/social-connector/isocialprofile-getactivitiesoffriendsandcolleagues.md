---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Este método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770870"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Este método foi preterido no Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Comentários

Iniciando no Outlook Social Connector 2013, o OSC suporta apenas sob demanda sincronização de atividades e não em cache ou sincronização híbrida das atividades. O OSC ignora a configuração de **cacheActivities** nos recursos de XML e não são mais chama esse método. Para dar suporte à pesquisa de atividades dinâmico, implemente o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Definir **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso. 
  
Para obter mais informações sobre como o OSC obtém atividades dos amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Confira também

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)


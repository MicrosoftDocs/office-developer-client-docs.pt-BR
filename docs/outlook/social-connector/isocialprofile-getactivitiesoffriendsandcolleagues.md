---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Esse método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406889"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a>ISocialProfile::GetActivitiesOfFriendsAndColleagues

Esse método foi preterido no Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a>Comentários

A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não sincronização híbrida ou em cache de atividades. O OSC ignora a **configuração cacheActivities** no XML de recursos e não chama mais esse método. Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2::GetActivitiesEx.](isocialsession2-getactivitiesex.md) Definir **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2::GetActivitiesEx** em vez disso. 
  
Para obter mais informações sobre como o OSC obtém atividades de amigos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md) 
  
## <a name="see-also"></a>Confira também

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)


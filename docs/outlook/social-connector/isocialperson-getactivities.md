---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Esse método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437739"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Esse método foi preterido no Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Comentários

A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e não em cache ou sincronização híbrida de atividades. O OSC ignora a configuração **cacheActivities** no XML Capabilities e não chama esse método. Para dar suporte à pesquisa de atividades dinâmicas, implemente o método [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) . Defina **cacheActivities** como **false**, **getactivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chame **ISocialSession2:: GetActivitiesEx** em vez disso. 
  
Para obter mais informações sobre como o OSC Obtém as atividades dos amigos, confira [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)


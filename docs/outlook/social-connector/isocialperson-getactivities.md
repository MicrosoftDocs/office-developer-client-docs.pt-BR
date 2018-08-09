---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Este método foi preterido no Outlook Social Connector 2013.
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770832"
---
# <a name="isocialpersongetactivities"></a>ISocialPerson::GetActivities

Este método foi preterido no Outlook Social Connector 2013.
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a>Comentários

Iniciando no Outlook Social Connector 2013, o OSC suporta apenas sob demanda sincronização de atividades e não em cache ou sincronização híbrida das atividades. O OSC ignora a configuração de **cacheActivities** nos recursos de XML e não chamar este método. Para dar suporte à pesquisa de atividades dinâmico, implemente o método [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) . Defina **cacheActivities** como **false**, **getActivities** e **dynamicActivitiesLookupEx** como **true**, que solicitará que o OSC chamada **ISocialSession2::GetActivitiesEx** em vez disso. 
  
Para obter mais informações sobre como o OSC obtém atividades dos amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md). 
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)


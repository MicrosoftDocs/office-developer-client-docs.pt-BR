---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321312"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém as condições para as quais os retornos de chamada são compatíveis com um objeto offline.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parâmetros

 _pulCapablities_
  
> bota Uma bitmask dos seguintes sinalizadores de recurso:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> O objeto offline é capaz de fornecer notificações offline.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> O objeto offline é capaz de fornecer notificações online.
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando o **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar no [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface do **IMAPIOffline** e chamar **IMAPIOffline:: GetCapabilities** para descobrir os retornos de chamada suportados pelo objeto. O cliente pode optar por configurar os retornos de chamada usando o **IMAPIOfflineMgr**.
  
Observe que, dependendo do servidor de email para um objeto offline, um objeto que oferece suporte a retornos de chamada para ficar online não necessariamente oferece suporte a retornos de chamada para ficar offline.
  
Observe também que, enquanto um objeto offline pode dar suporte a retornos de chamada para alterações diferentes de online/offline, a API de estado offline oferece suporte somente a alterações online/offline, e os clientes devem verificar apenas esses recursos.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)


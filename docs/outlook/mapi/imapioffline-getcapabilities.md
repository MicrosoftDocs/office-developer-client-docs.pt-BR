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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572029"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém as condições para o qual os retornos de chamada são suportados por um objeto offline.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parâmetros

 _pulCapablities_
  
> [out] Uma bitmask dos sinalizadores de recurso a seguir:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> O objeto offline é capaz de fornecer notificações offline.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> O objeto offline é capaz de fornecer notificações online.
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar em [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface **IMAPIOffline** e chamadas **IMAPIOffline::GetCapabilities** para descobrir os retornos de chamada com suporte pelo objeto. O cliente pode optar por configurar retornos de chamada usando **IMAPIOfflineMgr**.
  
Observe que, dependendo do servidor de email para um objeto offline, um objeto que oferece suporte a retornos de chamada para o modo online não necessariamente suporta retornos de chamada para entrar no modo offline.
  
Observe também que, enquanto um objeto offline pode suportar retornos de chamada para alterações que não seja online offline, a API de estado Offline suporta apenas alterações online offline e os clientes precisam verificar para apenas esses recursos.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes de MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)


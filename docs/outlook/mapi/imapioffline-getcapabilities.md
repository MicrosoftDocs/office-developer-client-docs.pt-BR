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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 205c9dd28692592ddf133b1b30989ba9fd4236f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767104"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Aplica-se a**: Outlook 
  
Obtém as condições para o qual os retornos de chamada são suportados por um objeto offline.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Par�metros

 _pulCapablities_
  
> [out] Uma bitmask dos sinalizadores de recurso a seguir:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> O objeto offline é capaz de fornecer notificações offline.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> O objeto offline é capaz de fornecer notificações online.
    
## <a name="remarks"></a>Coment�rios

Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar em [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface **IMAPIOffline** e chamadas **IMAPIOffline::GetCapabilities** para descobrir os retornos de chamada com suporte pelo objeto. O cliente pode optar por configurar retornos de chamada usando **IMAPIOfflineMgr**.
  
Observe que, dependendo do servidor de email para um objeto offline, um objeto que oferece suporte a retornos de chamada para o modo online não necessariamente suporta retornos de chamada para entrar no modo offline.
  
Observe também que, enquanto um objeto offline pode suportar retornos de chamada para alterações que não seja online offline, a API de estado Offline suporta apenas alterações online offline e os clientes precisam verificar para apenas esses recursos.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)


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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433371"
---
# <a name="imapiofflinegetcapabilities"></a>IMAPIOffline::GetCapabilities

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém as condições para as quais os retornos de chamada são suportados por um objeto offline.
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a>Parâmetros

 _porqueCapablities_
  
> [out] Uma máscara de bits dos seguintes sinalizadores de funcionalidade:
    
MAPIOFFLINE_CAPABILITY_OFFLINE
  
> O objeto offline é capaz de fornecer notificações offline.
    
MAPIOFFLINE_CAPABILITY_ONLINE
  
> O objeto offline é capaz de fornecer notificações online.
    
## <a name="remarks"></a>Comentários

Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente pode consultar [em IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) para obter um ponteiro para uma interface **IMAPIOffline** e chamar **IMAPIOffline::GetCapabilities** para descobrir os retornos de chamada suportados pelo objeto. O cliente pode optar por configurar retornos de chamada usando **IMAPIOfflineMgr**.
  
Observe que, dependendo do servidor de email para um objeto offline, um objeto que dá suporte a retornos de chamada para ficar online não necessariamente oferece suporte a retornos de chamada para ficar offline.
  
Observe também que, embora um objeto offline possa dar suporte a retornos de chamada para alterações diferentes de online/offline, a API de Estado Offline oferece suporte somente a alterações online/offline, e os clientes devem verificar apenas esses recursos.
  
## <a name="see-also"></a>Confira também



[IMAPIOffline::GetCurrentState](imapioffline-getcurrentstate.md)
  
[IMAPIOffline::SetCurrentState](imapioffline-setcurrentstate.md)
  
[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)


---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414764"
---
# <a name="mapioffline_notify"></a>MAPIOFFLINE_NOTIFY

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta é a notificação para uma alteração no estado da conexão. Ele indica a parte do estado de conexão que mudou, o estado de conexão antigo e o novo estado de conexão.
  
## <a name="quick-info"></a>Informações rápidas

Consulte **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a>Members

 _ulSize_
  
> Tamanho da estrutura **MAPIOFFLINE_NOTIFY** tamanho. 
    
 _NotifyType_
  
> Tipo de notificação. Observe que somente a notificação sobre a alteração do estado da conexão é suportada; os únicos valores com suporte são:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Um token definido pelo cliente na estrutura **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> A parte do estado de conexão que foi alterada. O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> O estado de conexão antigo. Os únicos valores com suporte são:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> O novo estado de conexão. Os únicos valores com suporte são:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Comentários

A API de Estado Offline é compatível apenas com notificações para alterações online/offline. Um cliente deve verificar se o Outlook retorna os seguintes valores antes de examinar a alteração real:
  
1.  *NotifyType*  tem o valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. Nesse caso, o cliente pode assumir que a alteração é uma alteração de estado de conexão, e  *Info*  é da estrutura  *StateChange*  . 
    
2.  *ulMask*  tem o valor MAPIOFFLINE_STATE_OFFLINE_MASK. Nesse caso, o cliente pode presumir que a alteração é uma alteração de estado de conexão online/offline e pode continuar examinando  *ulStateOld*  e  *ulStateNew*  . 
    
É possível que o Outlook notifique um cliente sobre outras alterações que não são suportadas. Nesses casos, *NotifyType* não seria qualquer um dos três valores declarados anteriormente ou *ulMask* não seria MAPIOFFLINE_STATE_OFFLINE_MASK, e o cliente deve ignorar o restante dos dados em *Informações.* 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de estado offline](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)


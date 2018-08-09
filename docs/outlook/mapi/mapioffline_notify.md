---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9d8eb3f2c52f20ffe57d84823a0ed736337b4d9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768008"
---
# <a name="mapiofflinenotify"></a>MAPIOFFLINE_NOTIFY

**Aplica-se a**: Outlook 
  
Esta é a notificação para uma alteração no estado de conexão. Indica a parte do estado de conexão que foi alterada, o estado de conexão antigo e o novo estado de conexão.
  
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
  
> Tamanho da estrutura **MAPIOFFLINE_NOTIFY** . 
    
 _NotifyType_
  
> Tipo de notificação. Observe que apenas notificação em alterar o estado de conexão é suportada; os únicos valores suportados são:
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE
    
   - MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE
    
 _ulClientToken_
  
> Um token definido pelo cliente na estrutura de **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** em **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
    
 _ulMask_
  
> A parte do estado de conexão que foi alterada. O único valor com suporte é MAPIOFFLINE_STATE_OFFLINE_MASK.
    
 _ulStateOld_
  
> O estado de conexão antigo. Os únicos valores suportados são:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
 _ulStateNew_
  
> O novo estado de conexão. Os únicos valores suportados são:
    
   - MAPIOFFLINE_STATE_OFFLINE
    
   - MAPIOFFLINE_STATE_ONLINE
    
## <a name="remarks"></a>Comentários

A API de estado Offline suporta somente notificações para alterações online offline. Um cliente deve verificar se o Outlook retorna os seguintes valores antes de examinar a alteração real:
  
1.  *NotifyType* tem o valor MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE ou MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE. Nesse caso, o cliente pode pressupõem que a alteração é uma alteração de estado de conexão, e *Info* da estrutura *estadoAlterar* . 
    
2.  *ulMask* tem o valor MAPIOFFLINE_STATE_OFFLINE_MASK. Nesse caso, o cliente pode pressupõem que a alteração é uma alteração de estado de conexão online offline e pode continuar com examinando *ulStateOld* e *ulStateNew* . 
    
É possível que o Outlook notifica um cliente de outras alterações que não são suportados. Nesses casos, *NotifyType* não seria qualquer um dos três valores mencionado anteriormente, ou *ulMask* não seria MAPIOFFLINE_STATE_OFFLINE_MASK e o cliente deve ignorar o restante dos dados em *Info* . 
  
## <a name="see-also"></a>Confira também

- [Sobre a API de estado offline](about-the-offline-state-api.md)  
- [Constantes MAPI](mapi-constants.md)  
- [MAPIOFFLINE_NOTIFY_TYPE](mapioffline_notify_type.md)


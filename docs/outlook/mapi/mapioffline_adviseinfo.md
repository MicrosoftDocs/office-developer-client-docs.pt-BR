---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565092"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações para **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** para registrar o retorno de chamada para um objeto offline. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte **IMAPIOfflineMgr::Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>Members

_ulSize_: O tamanho do **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: um token definido pelo cliente sobre um retorno de chamada. É o membro *ulClientToken* da estrutura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** passado para **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: tipo de retorno de chamada para fazer.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - O tipo de retorno de chamada é por notificação. Este é o único tipo com suporte de retorno de chamada.  *pCallback* deve indicar a interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: Interface para usar o retorno de chamada. Esta é a implementação do cliente de **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_ulAdviseTypes_: os tipos de advise, conforme identificado pela condição para que informa. O único tipo com suporte é MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: O único estado com suporte é MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Confira também

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Sobre a API de estado offline](about-the-offline-state-api.md) 
- [Constantes de MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)


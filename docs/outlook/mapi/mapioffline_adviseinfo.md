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
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420021"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações para **[IMAPIOfflineMgr:: avisar](imapiofflinemgr-advise.md)** para registrar retorno de chamada para um objeto offline. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte **IMAPIOfflineMgr:: Advise**. 
  
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

_ulSize_: o tamanho de **MAPIOFFLINE_ADVISEINFO**. 
    
_ulClientToken_: um token definido pelo cliente sobre um retorno de chamada. É o membro *ulClientToken* da estrutura **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** passada para **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)**. 
    
_CallbackType_: tipo de retorno de chamada a ser feita.
    
   -  MAPIOFFLINE_CALLBACK_TYPE_NOTIFY 
    
   - O tipo de retorno de chamada é por notificação. Este é o único tipo de retorno de chamada com suporte.  *pCallback* deve indicar a interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
_pCallback_: interface a ser usada para retorno de chamada. Esta é a implementação do **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** do cliente. 
    
_ulAdviseTypes_: os tipos de aviso, conforme identificado pela condição de aconselhação. O único tipo com suporte é MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.
    
_ulStateMask_: o único estado com suporte é MAPIOFFLINE_STATE_ALL.
    
## <a name="see-also"></a>Confira também

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Sobre a API de estado offline](about-the-offline-state-api.md) 
- [Constantes MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)


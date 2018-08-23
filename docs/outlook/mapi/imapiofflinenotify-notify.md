---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: a84114a3363f9cbcd9455bce12d3171843bd18a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571112"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia notificações para o cliente sobre alterações no estado da conexão.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parâmetros

 _pNotifyInfo_
  
> [in] A notificação informando que o Outlook enviará ao cliente. A notificação indica a parte do estado de conexão que foi alterada, o estado de conexão antigo e o novo estado de conexão.
    
## <a name="remarks"></a>Comentários

O Outlook usa este método para enviar retornos de chamada de notificação para um cliente. Para disponibilizar essa interface para Microsoft Outlook 2010 ou o Microsoft Outlook 2013, o cliente deve implementar essa interface e passar um ponteiro para ele como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
O cliente também passa para **MAPIOFFLINE_ADVISEINFO** um token de cliente que o Outlook 2010 ou Outlook 2013 usa **IMAPIOfflineNotify::Notify** para identificar o cliente registrado para o retorno de chamada de notificação. 
  
Em geral, o Outlook 2010 e o Outlook 2013 podem notificá-um cliente de alterações online offline e outras alterações de estado de conexão, mas a API de estado Offline dá suporte a notificações apenas para alterações online offline. O cliente deve ignorar todos os outras notificações.
  
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)


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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410690"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia notificações ao cliente sobre alterações no estado da conexão.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parâmetros

 _pNotifyInfo_
  
> [in] A notificação que o Outlook envia ao cliente. A notificação indica a parte do estado de conexão que mudou, o estado de conexão antigo e o novo estado de conexão.
    
## <a name="remarks"></a>Comentários

O Outlook usa esse método para enviar retornos de chamada de notificação para um cliente. Para disponibilizar essa interface para o Microsoft Outlook 2010 ou o Microsoft Outlook 2013, o cliente deve implementar essa interface e passar um ponteiro para ela como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
  
O cliente também passa para **MAPIOFFLINE_ADVISEINFO** um token de cliente que o Outlook 2010 ou o Outlook 2013 usa em **IMAPIOfflineNotify::Notify** para identificar o cliente registrado para o retorno de chamada de notificação. 
  
In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes. O cliente deve ignorar todas as outras notificações.
  
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)


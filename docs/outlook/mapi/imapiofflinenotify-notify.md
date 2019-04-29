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
  
Envia notificações ao cliente sobre alterações no estado de conexão.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parâmetros

 _pNotifyInfo_
  
> no A notificação que o Outlook envia ao cliente. A notificação indica a parte do estado de conexão que foi alterada, o estado de conexão antigo e o estado da nova conexão.
    
## <a name="remarks"></a>Comentários

O Outlook usa este método para enviar retornos de chamada de notificação para um cliente. Para tornar esta interface disponível para o Microsoft Outlook 2010 ou o Microsoft Outlook 2013, o cliente deve implementar essa interface e passar um ponteiro para ela como membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar os retornos de chamada usando o **[IMAPIOfflineMgr:: Advise ](imapiofflinemgr-advise.md)**. 
  
O cliente também passa para o **MAPIOFFLINE_ADVISEINFO** um token de cliente que o Outlook 2010 ou o Outlook 2013 usa no **IMAPIOfflineNotify:: notifique** para identificar o cliente registrado para o retorno de chamada de notificação. 
  
Em geral, o Outlook 2010 e o Outlook 2013 podem notificar um cliente sobre alterações online/offline e outras alterações de estado de conexão, mas a API de estado offline suporta apenas notificações para alterações online/offline. O cliente deve ignorar todas as outras notificações.
  
## <a name="see-also"></a>Confira também



[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)


---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435933"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia uma notificação de um evento especificado para uma fonte de aviso que originalmente registrada para a notificação por meio do [método IMAPISupport::Subscribe.](imapisupport-subscribe.md) 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

_lpKey_
  
> [in] Um ponteiro para a tecla de notificação para o objeto de origem de aviso. O  _parâmetro lpKey_ não pode ser NULL. 
    
_cNotification_
  
> [in] A contagem de estruturas de notificação apontadas pelo _parâmetro lpNotifications._ 
    
_lpNotifications_
  
> [in] Um ponteiro para uma matriz de [estruturas NOTIFICATION](notification.md) que descrevem notificações pendentes. 
    
_lpulFlags_
  
> [in, out] Uma máscara de bits de sinalizadores que controla o processo de notificação. Na entrada, o sinalizador a seguir pode ser definido:
    
  - MAPI_UNICODE 
    
    > As cadeias de caracteres nas estruturas de notificação apontadas por  _lpNotifications_ estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 

    Na saída, MAPI pode definir o seguinte sinalizador:
        
  - NOTIFY_CANCELED 
    
    > Uma função de retorno de chamada cancelou uma notificação síncrona.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As notificações foram geradas com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::Notify** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam Notify **para** solicitar que o MAPI gere uma notificação para um sink de aviso que já foi registrado para a notificação por meio do método **IMAPISupport::Subscribe.** 
  
**Notificar** copia as estruturas apontadas pelo parâmetro  _lpNotifications_ na memória e chama o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do pia apropriado. Quando **OnNotify** é concluído com a notificação, ele libera a memória envolvida. O chamador não precisa alocar memória; O MAPI executa toda a alocação de memória necessária. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A chave de notificação passada _no parâmetro lpKey_ deve ser idêntica à chave passada _em lpKey_ para o **método IMAPISupport::Subscribe.** Muitos provedores usam o identificador de entrada da fonte de consultoria como a chave, mas outros dados, como um caminho de arquivo, podem ser usados. MAPI uses this key to find all the registrations for notifications on the identified advise source. 
  
Certifique-se de definir o **membro lpEntryID** da estrutura de notificação como um identificador de entrada de longo prazo. 
  
Se você definir o sinalizador NOTIFY_SYNC  na chamada subscribe para qualquer uma das notificações pendentes,  notificar chama as funções de retorno de chamada do método **IMAPIAdviseSink::OnNotify** antes de retornar. Um sink advise pode ser criado manualmente ou chamando [HrAllocAdviseSink](hrallocadvisesink.md). A **função HrAllocAdviseSink** permite que seu chamador  especifique uma função de retorno de chamada que notifique chamadas como parte da notificação. A função de retorno de chamada está em conformidade com o protótipo [NOTIFCALLBACK.](notifcallback.md) As funções de retorno de chamada implementadas pelos clientes sempre retornam S_OK; as funções de retorno de chamada implementadas pelos provedores de serviços podem retornar CALLBACK_DISCONTINUE. 
  
Se uma função de retorno de chamada retornar CALLBACK_DISCONTINUE, MAPI para de enviar notificações e retorna NOTIFY_CANCELED no parâmetro _lpulFlags_ do método **Notify.** Você pode presumir que o processo está inativo e parar de gerar notificações para esse processo. Se **Notificar** retornar 0 em  _lpulFlags_, o processo ainda está ativo e você deve continuar a enviar notificações, conforme apropriado.
  
Ao usar notificações síncronas, tenha cuidado para evitar situações de deadlock.
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [NOTIFICAÇÃO](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriedade canônica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326366"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia uma notificação de um evento especificado para uma fonte de aviso registrada originalmente para a notificação por meio do método [IMAPISupport:: Subscribe](imapisupport-subscribe.md) . 
  
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
  
> no Um ponteiro para a chave de notificação para o objeto de origem de aviso. O parâmetro _lpKey_ não pode ser nulo. 
    
_cNotification_
  
> no A contagem de estruturas de notificação apontadas pelo parâmetro _lpNotifications_ . 
    
_lpNotifications_
  
> no Um ponteiro para uma matriz de estruturas de [notificação](notification.md) que descrevem as notificações pendentes. 
    
_lpulFlags_
  
> [in, out] Uma bitmask de sinalizadores que controlam o processo de notificação. Na entrada, o seguinte sinalizador pode ser definido:
    
  - MAPI_UNICODE 
    
    > As cadeias de caracteres nas estruturas de notificação apontadas pelo _lpNotifications_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 

    Na saída, o MAPI pode definir o seguinte sinalizador:
        
  - NOTIFY_CANCELED 
    
    > Uma função de retorno de chamada cancelou uma notificação síncrona.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As notificações foram geradas com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: Notify** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de **** serviços de chamadas notificam para solicitar que o MAPI gere uma notificação para um coletor de aviso registrado anteriormente para a notificação através do método **IMAPISupport:: Subscribe** . 
  
**Notify** copia as estruturas apontadas pelo parâmetro _lpNotifications_ para a memória e chama o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de avisos apropriado. Quando **OnNotify** é concluído com a notificação, ele libera a memória envolvida. O chamador não precisa alocar memória; O MAPI realiza todas as alocações de memória necessárias. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A chave de notificação passada no parâmetro _lpKey_ deve ser idêntica à chave passada em _lpKey_ para o método **IMAPISupport:: Subscribe** . Muitos provedores usam o identificador de entrada da fonte de aviso como a chave, mas outros dados, como um caminho de arquivo, podem ser usados. O MAPI usa essa chave para localizar todos os registros de notificações na fonte de aviso identificada. 
  
Certifique-se de definir o membro **lpEntryID** da estrutura de notificação para um identificador de entrada de longo prazo. 
  
Se você definir o sinalizador NOTIFY_SYNC na chamada **Subscribe** para qualquer uma das notificações pendentes, **notifique** as chamadas as funções de retorno de chamada do método **IMAPIAdviseSink:: OnNotify** antes de retornar. Um coletor de aviso pode ser criado manualmente ou chamando [HrAllocAdviseSink](hrallocadvisesink.md). A função **HrAllocAdviseSink** permite que o chamador especifique uma função de retorno de chamada que **notifique** as chamadas como parte da notificação. A função de retorno de chamada está em conformidade com o protótipo [NOTIFCALLBACK](notifcallback.md) . As funções de retorno de chamada implementadas por clientes sempre retornam S_OK; as funções de retorno de chamada implementadas por provedores de serviços podem retornar CALLBACK_DISCONTINUE. 
  
Se uma função de retorno de chamada retornar CALLBACK_DISCONTINUE, o MAPI interromperá o envio de notificações e retornará NOTIFY_CANCELED no parâmetro _lpulFlags_ do método **Notify** . Você pode supor que o processo está inativo e parar de gerar notificações para esse processo. Se **notificar** retornar 0 no _lpulFlags_, o processo ainda estará ativo e você deverá continuar a enviar notificações, conforme apropriado.
  
Ao usar notificações síncronas, tenha cuidado para evitar situações de deadlock.
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [NOTIFICATION](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriedade canônica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)


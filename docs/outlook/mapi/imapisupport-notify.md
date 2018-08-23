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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572036"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Envia uma notificação de um evento especificado a uma fonte de advise originalmente registrado para a notificação por meio do método [IMAPISupport::Subscribe](imapisupport-subscribe.md) . 
  
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
  
> [in] Um ponteiro para a chave de notificação para o objeto de origem advise. O parâmetro _lpKey_ não pode ser NULL. 
    
_cNotification_
  
> [in] A contagem de estruturas de notificação apontado pelo parâmetro _lpNotifications_ . 
    
_lpNotifications_
  
> [in] Um ponteiro para uma matriz de estruturas de [notificação](notification.md) que descrevem notificações pendentes. 
    
_lpulFlags_
  
> [além, out] Uma bitmask dos sinalizadores que controla o processo de notificação. Na entrada, o seguinte sinalizador pode ser definido:
    
  - MAPI_UNICODE 
    
    > As cadeias de caracteres nas estruturas notificação apontadas pela _lpNotifications_ estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 

    Na saída, MAPI pode definir o sinalizador a seguir:
        
  - NOTIFY_CANCELED 
    
    > Uma função de retorno de chamada foi cancelada uma notificação síncrona.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As notificações foram geradas com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::Notify** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de chamarem **Notify** para solicitar que o MAPI gerar uma notificação para um coletor de advise foi registrado anteriormente para a notificação por meio do método **IMAPISupport::Subscribe** . 
  
**Notificar** cópias as estruturas apontado pelo parâmetro _lpNotifications_ na memória e chama o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise apropriado. Quando **OnNotify** for concluído com a notificação, ele libera a memória envolvidos. O chamador não precisa alocar memória; MAPI executa todos os alocação de memória necessárias. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A chave de notificação passada no parâmetro _lpKey_ deve ser idêntica à chave _lpKey_ passado ao método **IMAPISupport::Subscribe** . Muitos provedores de usam o identificador de entrada da fonte de advise como a chave, mas outros dados, por exemplo, um caminho de arquivo, que podem ser usados. MAPI usa essa chave para localizar todos os registros de notificações na fonte de advise identificados. 
  
Certifique-se de que você defina o membro **lpEntryID** da estrutura de notificação para um identificador de entrada de longo prazo. 
  
Se você definir o sinalizador NOTIFY_SYNC no **Subscribe** chamada para qualquer uma das notificações de pendente, você deverá **Notificar** chamadas as funções de retorno de chamada do método **IMAPIAdviseSink::OnNotify** antes de retornar. Um coletor de advise pode ser criado manualmente ou chamando [HrAllocAdviseSink](hrallocadvisesink.md). A função **HrAllocAdviseSink** permite que o seu chamador especificar uma função de retorno de chamada que chamadas **Notify** como parte da notificação. A função de retorno de chamada está de acordo com o protótipo [NOTIFCALLBACK](notifcallback.md) . Funções de retorno de chamada implementadas pelos clientes sempre retornam S_OK; funções de retorno de chamada implementadas pelos provedores de serviços podem retornar CALLBACK_DISCONTINUE. 
  
Se uma função de retorno de chamada retorna CALLBACK_DISCONTINUE, MAPI interrompe o envio de notificações e retorna NOTIFY_CANCELED no parâmetro de _lpulFlags_ do método **Notify** . Você pode assumir que o processo está inativa e interromper gerar notificações para esse processo. Se **Notify** retorna 0 em _lpulFlags_, o processo ainda está ativo e você deve continuar a enviar notificações, conforme apropriado.
  
Quando você usa notificações síncronas, tome cuidado para evitar situações de deadlock.
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [NOTIFICAÇÃO](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [Propriedade canônica PidTagRecordKey](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)


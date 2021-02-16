---
title: IABLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Unadvise
api_type:
- COM
ms.assetid: 3e506b29-c7e3-40d6-a08b-22fa87088c2d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fe87de4466413e317edea5d358c9e4769d0c5593
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424074"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela notificações que foram configuradas anteriormente com uma chamada para o [método IABLogon::Advise.](iablogon-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> [in] O número de conexão associado a um registro de notificação ativo. Uma chamada anterior para **Advise** deve ter retornado o valor  _de ulConnection_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

MAPI calls the **Unadvise** method to cancel a notification registration for a container, messaging user, or distribution list object. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Sua implementação do **Unadvise dependerá** de você dar suporte à notificação com a ajuda de MAPI ou manualmente. Se o MAPI oferece suporte, chame o [método IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar o registro. Se outro thread estiver no processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do cliente, ele poderá ser atrasado até que **OnNotify** seja retornado. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de Evento em MAPI](event-notification-in-mapi.md). For information about how to use the [IMAPISupport : IUnknown](imapisupportiunknown.md) methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).
  
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)


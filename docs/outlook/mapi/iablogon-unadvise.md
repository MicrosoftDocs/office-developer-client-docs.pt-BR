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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3fbf8b423cfd4206a0143b5639c85dbcacce2fae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570979"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela notificações que foram definidas com uma chamada ao método [IABLogon::Advise](iablogon-advise.md) anteriormente. 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] O número de conexão associado a um registro de notificação ativo. Uma chamada anterior a **Advise** deve ter retornado o valor de _ulConnection_.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro de notificação foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **Unadvise** para cancelar um registro de notificação para um contêiner, usuário ou objeto de lista de distribuição de mensagens. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

A implementação dos **Unadvise** dependerá se você oferecer suporte a notificação com a Ajuda do MAPI ou manualmente. Se MAPI fornece seu suporte, chame o método de [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md) para cancelar o registro. Se outro thread no processo de chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise, ela pode ser atrasada até **OnNotify** ter retornado. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações sobre como usar o [IMAPISupport: IUnknown](imapisupportiunknown.md) métodos para dar suporte a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).
  
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)


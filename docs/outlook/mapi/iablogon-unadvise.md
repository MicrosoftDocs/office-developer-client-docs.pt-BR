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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348878"
---
# <a name="iablogonunadvise"></a>IABLogon::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela as notificações que foram configuradas anteriormente com uma chamada para o método [IABLogon:: Advise](iablogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> no O número de conexão associado a um registro de notificação ativo. Uma chamada anterior para **Advise** deve ter retornado o valor de _ulConnection_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro de notificação foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

MAPI chama o método **Unadvise** para cancelar um registro de notificação para um contêiner, usuário de mensagens ou objeto de lista de distribuição. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação de **Unadvise** dependerá se você dá suporte à notificação com a ajuda do MAPI ou manualmente. Se o MAPI fornecer seu suporte, chame o método [IMAPISupport:: unsubscribe](imapisupport-unsubscribe.md) para cancelar o registro. Se outro thread estiver no processo de chamar o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) do coletor de aviso, ele poderá ser adiado **** até que OnNotify tenha sido retornado. 
  
Para obter mais informações sobre o processo de notificação, consulte [Event Notification in MAPI](event-notification-in-mapi.md). Para obter informações sobre como usar os métodos [IMAPISupport: IUnknown](imapisupportiunknown.md) para dar suporte à notificação, consulte [support Event Notification](supporting-event-notification.md).
  
## <a name="see-also"></a>Confira também



[IABLogon::Advise](iablogon-advise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)


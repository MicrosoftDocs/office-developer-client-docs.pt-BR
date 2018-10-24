---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 73a4c07c69fb10044cba6e9368cd4bc86c11ad54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575067"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa o armazenamento de mensagens que uma nova mensagem chegou. Este método é chamado somente pelo spooler MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parâmetros

 _lpNotification_
  
> [in] Um ponteiro para uma estrutura de [notificação](notification.md) que descreve a notificação de mensagem nova. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O armazenamento de mensagens foi notificado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::NotifyNewMail** é chamado pelo spooler MAPI para informar o armazenamento de mensagens que uma mensagem está pronta para entrega. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando **NotifyNewMail** é chamado, envie uma notificação de novo email para todos os clientes registrados. Você pode enviar a notificação chamando [IMAPISupport::Notify](imapisupport-notify.md), se você optar por usar os métodos do objeto de suporte ou usando sua própria implementação. Um cliente registrado é aquele que tem chamado [IMsgStore::Advise](imsgstore-advise.md) e defina o parâmetro _lpEntryID_ como nulo e o parâmetro _ulEventMask_ para _fnevNewMail_. 
  
Não modifique ou liberar a memória para a estrutura de [notificação](notification.md) que descreve a notificação de mensagem nova. Copie a estrutura de **notificação** chamando a função do utilitário [ScCopyNotifications](sccopynotifications.md) para fazer uso das informações em seus membros. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[NOTIFICATION](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


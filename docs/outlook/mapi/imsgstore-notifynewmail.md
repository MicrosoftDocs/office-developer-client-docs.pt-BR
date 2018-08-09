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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bdda950cd1fab66db46590e0b9141bb3d2a75221
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767493"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Aplica-se a**: Outlook 
  
Informa o armazenamento de mensagens que uma nova mensagem chegou. Este método é chamado somente pelo spooler MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parâmetros

 _lpNotification_
  
> [in] Um ponteiro para uma estrutura de [notificação](notification.md) que descreve a notificação de mensagem nova. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O armazenamento de mensagens foi notificado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::NotifyNewMail** é chamado pelo spooler MAPI para informar o armazenamento de mensagens que uma mensagem está pronta para entrega. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando **NotifyNewMail** é chamado, envie uma notificação de novo email para todos os clientes registrados. Você pode enviar a notificação chamando [IMAPISupport::Notify](imapisupport-notify.md), se você optar por usar os métodos do objeto de suporte ou usando sua própria implementação. Um cliente registrado é aquele que tem chamado [IMsgStore::Advise](imsgstore-advise.md) e defina o parâmetro _lpEntryID_ como nulo e o parâmetro _ulEventMask_ para _fnevNewMail_. 
  
Não modifique ou liberar a memória para a estrutura de [notificação](notification.md) que descreve a notificação de mensagem nova. Copie a estrutura de **notificação** chamando a função do utilitário [ScCopyNotifications](sccopynotifications.md) para fazer uso das informações em seus membros. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[NOTIFICAÇÃO](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


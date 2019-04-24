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
ms.openlocfilehash: a8ec06fd0401a129e08a06acdb1c18785f90d4a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348752"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa ao repositório de mensagens que uma nova mensagem chegou. Este método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parâmetros

 _lpNotification_
  
> no Um ponteiro para uma estrutura de [notificação](notification.md) que descreve a nova notificação de mensagem. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O repositório de mensagens foi notificado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: NotifyNewMail** é chamado pelo spooler MAPI para informar ao armazenamento de mensagens que uma mensagem está pronta para entrega. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando **NotifyNewMail** é chamado, envie uma nova notificação de email a todos os clientes registrados. Você pode enviar a notificação chamando [IMAPISupport:: Notify](imapisupport-notify.md), se você optar por usar os métodos do objeto support ou usando sua própria implementação. Um cliente registrado é um que chamou [IMsgStore:: Advise](imsgstore-advise.md) e define o parâmetro _lpEntryID_ como nulo e o parâmetro _ulEventMask_ como _fnevNewMail_. 
  
Não modifique ou libere a memória da estrutura de [notificação](notification.md) que descreve a notificação de novo email. Copie a estrutura de **notificação** chamando a função do utilitário [ScCopyNotifications](sccopynotifications.md) para fazer uso das informações em seus membros. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[NOTIFICATION](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


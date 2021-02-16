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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431775"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::NotifyNewMail

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informa ao armazenamento de mensagens que uma nova mensagem chegou. Esse método é chamado apenas pelo spooler MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Parâmetros

 _lpNotification_
  
> [in] Um ponteiro para uma [estrutura NOTIFICATION](notification.md) que descreve a nova notificação de mensagem. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O armazenamento de mensagens foi notificado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::NotifyNewMail** é chamado pelo spooler MAPI para informar ao repositório de mensagens que uma mensagem está pronta para entrega. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando **NotifyNewMail** for chamado, envie uma nova notificação por email para todos os clientes registrados. Você pode enviar a notificação chamando [IMAPISupport::Notify](imapisupport-notify.md), se você optar por usar os métodos de objeto de suporte ou usando sua própria implementação. Um cliente registrado é aquele que chamou [IMsgStore::Advise](imsgstore-advise.md) e definiu o parâmetro  _lpEntryID_ como NULL e o parâmetro  _ulEventMask_ como  _fnevNewMail_. 
  
Não modifique ou livre a memória para a estrutura [NOTIFICATION](notification.md) que descreve a nova notificação de email. Copie a **estrutura NOTIFICATION** chamando a função utilitária [ScCopyNotifications](sccopynotifications.md) para usar as informações em seus membros. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[NOTIFICAÇÃO](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430228"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela o envio de notificações configuradas anteriormente com uma chamada para o [método IMAPITable::Advise.](imapitable-advise.md) 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> [in] O número da conexão de registro retornada por uma chamada para [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Use o método **IMAPITable::Unadvise** para liberar o ponteiro para o objeto sink de aviso passado no parâmetro  _lpAdviseSink_ na chamada anterior para **IMAPITable::Advise**, cancelando assim um registro de notificação. Como parte do descarte do ponteiro para o objeto de pia de alerta, o método **IUnknown::Release** do objeto é chamado. Geralmente, **Release** é chamado durante a chamada **Unadvise,** mas se outro thread estiver em processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o sink de consultoria, a chamada **Release** será atrasada até que o método **OnNotify** retorne. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela.](about-table-notifications.md) Para obter informações sobre como usar os **métodos IMAPISupport** para dar suporte à notificação, consulte [Notificação de Evento de Suporte.](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI usa o **método IMAPITable::Unadvise** para cancelar notificações para a tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)


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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767360"
---
# <a name="imapitableunadvise"></a>IMAPITable::Unadvise

  
  
**Aplica-se a**: Outlook 
  
Cancela o envio de notificações configuradas anteriormente com uma chamada ao método [IMAPITable::Advise](imapitable-advise.md) . 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] O número da conexão de registro retornado por uma chamada para [IMAPITable::Advise](imapitable-advise.md).
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

Use o método **IMAPITable::Unadvise** para liberar o ponteiro para o objeto de coletor de eventos de advise passado no parâmetro _lpAdviseSink_ na chamada anterior a **IMAPITable::Advise**, assim, Cancelando um registro de notificação. Como parte do descartar o ponteiro para o objeto coletor de eventos advise, o método do objeto **IUnknown:: Release** é chamado. Geralmente, a **versão** é chamado durante a chamada **Unadvise** , mas se outro thread está em processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) para o coletor de advise, a chamada de **liberação** foi adiada até o **OnNotify** método retorna. 
  
Para obter mais informações sobre o processo de notificação, consulte [Notificação de evento em MAPI](event-notification-in-mapi.md). Para obter informações específicas sobre a notificação de tabela, consulte [Sobre notificações de tabela](about-table-notifications.md). Para obter informações sobre como usar os métodos **IMAPISupport** para suportar a notificação, consulte [Suporte a notificação de evento](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::NotificationOff  <br/> |MFCMAPI usa o método **IMAPITable::Unadvise** para cancelar as notificações para a tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Advise](imapitable-advise.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)


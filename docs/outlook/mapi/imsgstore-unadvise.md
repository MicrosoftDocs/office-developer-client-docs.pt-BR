---
title: IMsgStoreUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Unadvise
api_type:
- COM
ms.assetid: 1394039b-d509-49a5-8421-b7362d906879
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 516de39d721c532c003775bd366a52ed8144ab88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767533"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Aplica-se a**: Outlook 
  
Cancela o envio de notificações configuradas anteriormente com uma chamada ao método [IMsgStore::Advise](imsgstore-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] O número de conexão associado a um registro de notificação ativo. O valor de _ulConnection_ deve ter retornado por uma chamada anterior para o método **IMsgStore::Advise** . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::Unadvise** cancela um registro de notificação. Versões de **Unadvise** coletor, o que ele recebido na chamada **Advise** usada para o registro de aviso de seu ponteiro para o chamador. 
  
Geralmente, o **Unadvise** chama o método de [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) do coletor de eventos advise durante a chamada **Unadvise** . No entanto, se outro thread no processo de chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos advise, a chamada de **liberação** foi adiada até que o método **OnNotify** retorna. 
  
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


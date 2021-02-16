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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f85b662b7fe710c66a2e69dd3cd3db22e3283ddb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309720"
---
# <a name="imsgstoreunadvise"></a>IMsgStore::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela o envio de notificações configuradas anteriormente com uma chamada para o [método IMsgStore::Advise.](imsgstore-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> [in] O número de conexão associado a um registro de notificação ativo. O valor de _ulConnection_ deve ter sido retornado por uma chamada anterior para o **método IMsgStore::Advise.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::Unadvise** cancela um registro para notificação. **A unadvise** libera seu ponteiro para o pia de conselhos do chamador, que ele recebeu na chamada **Advise** usada para registro. 
  
Geralmente, **Unadvise** chama o método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do sink de consultoria durante **a chamada Unadvise.** No entanto, se outro thread estiver em processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do cliente de alerta, a chamada **release** será atrasada até que o método **OnNotify** retorne. 
  
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Advise](imsgstore-advise.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


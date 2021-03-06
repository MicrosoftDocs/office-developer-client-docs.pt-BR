---
title: IMAPISessionUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335697"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cancela o envio de notificações configuradas anteriormente com uma chamada para o [método IMAPISession::Advise.](imapisession-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> [in] Um número de conexão associado a um registro de notificação ativo. O valor de  _ulConnection_ deve ter sido retornado por uma chamada anterior para **IMAPISession::Advise**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro foi cancelado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::Unadvise** cancela um registro para notificação. **A unadvise** libera seu ponteiro para o pia de conselhos do chamador, que ele recebeu na chamada **Advise** usada para registro. 
  
Geralmente, **Unadvise** chama o método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do sink de aconselhe durante **a chamada Unadvise.** No entanto, se outro thread estiver em processo de chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do cliente de alerta, a chamada **release** será atrasada até que o método **OnNotify** retorne. 
  
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


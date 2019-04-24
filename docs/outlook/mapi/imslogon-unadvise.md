---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317273"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove o registro de um objeto para notificação de alterações de repositório de mensagens previamente estabelecidas usando uma chamada para o método [IMSLogon:: Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parâmetros

 _ulConnection_
  
> no O número da conexão de registro retornada por uma chamada para **IMSLogon:: Advise**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de repositório de mensagens implementam o método **IMSLogon:: Unadvise** para liberar o ponteiro para o objeto de coletor de aviso passado no parâmetro _lpAdviseSink_ na chamada anterior para **IMSLogon:: Advise**, cancelando uma notificação registro. Como parte de descartar o ponteiro para o objeto de coletor de aviso, o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto é chamado. Geralmente, o **lançamento** é chamado durante a chamada de **Unadvise** . However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns. 
  
## <a name="see-also"></a>Confira também



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


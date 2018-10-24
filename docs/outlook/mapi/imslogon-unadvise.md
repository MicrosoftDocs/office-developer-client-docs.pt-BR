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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387629"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove o registro de um objeto de notificação de alteração de repositório de mensagem tenha estabelecido por meio de uma chamada ao método [IMSLogon::Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Par�metros

 _ulConnection_
  
> [in] O número da conexão de registro retornado por uma chamada para **IMSLogon::Advise**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Mensagem armazenar provedores implementar o método **IMSLogon::Unadvise** para liberar o ponteiro para o objeto de coletor de eventos de advise passado no parâmetro _lpAdviseSink_ na chamada anterior a **IMSLogon::Advise**, cancelando, portanto, uma notificação Registro. Como parte do descartar o ponteiro para o objeto coletor de eventos advise, o método do objeto [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) é chamado. Geralmente, a **versão** é chamado durante a chamada **Unadvise** . However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns. 
  
## <a name="see-also"></a>Ver tamb�m



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


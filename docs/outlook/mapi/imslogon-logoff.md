---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399232"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Logs de uma mensagem armazenam provedor. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [in] Reservado; deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores de armazenamento de mensagem implementam o método **IMSLogon::Logoff** para serem desligados obrigatoriamente um provedor de armazenamento de mensagem. **IMSLogon::Logoff** é chamado nas seguintes situações: 
  
- Enquanto está fazendo logon fora de um cliente MAPI após uma chamada para o método [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Enquanto o MAPI é fazer logoff de um provedor de armazenamento de mensagem. Nesse caso, **IMSLogon::Logoff** é chamado como parte do MAPI processar o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto de suporte que o provedor de armazenamento de mensagem cria enquanto ele está processando uma [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou **IUnknown:: Versão** chamada de método em um objeto de repositório de mensagem. 
    
## <a name="see-also"></a>Confira também



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


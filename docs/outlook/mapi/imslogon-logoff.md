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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348871"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz o login de um provedor de armazenamento de mensagens. 
  
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
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de armazenamento de mensagens implementam o método **IMSLogon::Logoff** para forçar o desligado de um provedor de armazenamento de mensagens. **IMSLogon::Logoff** é chamado nas seguintes situações: 
  
- Enquanto o MAPI está fazendo logoff de um cliente após uma chamada para o [método IMAPISession::Logoff.](imapisession-logoff.md) 
    
- Enquanto o MAPI está fazendo logo off de um provedor de armazenamento de mensagens. Nesse caso, **IMSLogon::Logoff** é chamado como parte do processamento de MAPI do método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto de suporte que o provedor de repositório de mensagens cria durante o processamento de uma chamada de método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou **IUnknown::Release** em um objeto de repositório de mensagens. 
    
## <a name="see-also"></a>Confira também



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


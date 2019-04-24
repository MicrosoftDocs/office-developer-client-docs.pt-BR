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
  
Faz logoff de um provedor de repositório de mensagens. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> no Serve deve ser um ponteiro para zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de repositórios de mensagens implementam o método **IMSLogon:: logoff** para desligar forçosamente um provedor de armazenamento de mensagens. **IMSLogon:: logoff** é chamado nas seguintes situações: 
  
- Enquanto o MAPI estiver fazendo o logoff de um cliente após uma chamada para o método [IMAPISession:: logoff](imapisession-logoff.md) . 
    
- Embora o MAPI faça o logoff de um provedor de armazenamento de mensagens. Nesse caso, **IMSLogon:: logoff** é chamado como parte do processamento de MAPI o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto support que o provedor de repositório de mensagens cria enquanto processa um [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) ou **IUnknown:: **Chamada de método Release em um objeto do repositório de mensagens. 
    
## <a name="see-also"></a>Confira também



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)


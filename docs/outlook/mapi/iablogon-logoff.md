---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766842"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Aplica-se a**: Outlook 
  
Inicia o processo de logoff.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O processo de logoff foi iniciado com êxito.
    
## <a name="remarks"></a>Coment�rios

O processo de logoff geralmente é iniciado quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar uma sessão. MAPI, em seguida, chama o método **IABLogon::Logoff** do cada provedor catálogo de endereços para iniciar o processo de logoff. 
  
O método **IABLogon::Logoff** faz o seguinte: 
  
- Libera todos os objetos abertos, como qualquer subobjetos ou o objeto de status.
    
- Libera o objeto de suporte do provedor.
    
Para obter mais informações sobre o processo de logoff de provedores de catálogo de endereços, consulte [Sendo pressionada um provedor de serviços](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Confira também



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)


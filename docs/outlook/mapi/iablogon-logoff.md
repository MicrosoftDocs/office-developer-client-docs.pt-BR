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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339295"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia o processo de logoff.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de logoff foi iniciado com êxito.
    
## <a name="remarks"></a>Comentários

O processo de logoff normalmente é iniciado quando um cliente chama o método [IMAPISession:: logoff](imapisession-logoff.md) para finalizar uma sessão. Em seguida, o MAPI chama cada método **IABLogon:: logoff** do provedor de catálogo de endereços para iniciar o processo de logoff. 
  
O método **IABLogon:: logoff** faz o seguinte: 
  
- Libera todos os objetos abertos, como qualquer subobjeto ou o objeto status.
    
- Libera o objeto support do provedor.
    
Para obter mais informações sobre o processo de logoff dos provedores de catálogo de endereços, consulte desLigamento [de um provedor de serviços](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>Confira também



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)


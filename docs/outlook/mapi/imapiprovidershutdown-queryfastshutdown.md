---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418215"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Consulta o provedor MAPI para obter suporte para desligamento rápido. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O provedor MAPI dá suporte ao cliente MAPI para fazer desligamento rápido.
    
MAPI_E_NO_SUPPORT
  
> O provedor MAPI não dá suporte ao cliente MAPI para fazer desligamento rápido.
    
## <a name="remarks"></a>Comentários

Os provedores MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) e fazer com que o método **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** retorne MAPI_E_NO_SUPPORT. Para o Outlook como um cliente MAPI, isso faz com que o Outlook espere que todas as referências externas sejam liberadas antes de sair. 
  
Dependendo da configuração do registro do Windows do usuário para desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede um desligamento rápido do cliente. 
  
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


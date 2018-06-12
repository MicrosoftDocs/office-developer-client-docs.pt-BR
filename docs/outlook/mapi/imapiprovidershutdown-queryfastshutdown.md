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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767193"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a>IMAPIProviderShutdown::QueryFastShutdown

  
  
**Aplica-se a**: Outlook 
  
Suporte a consultas o provedor MAPI para o desligamento rápido. 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor retornado

S_OK
  
> O provedor MAPI suporta o cliente MAPI para rápida desligamento.
    
MAPI_E_NO_SUPPORT
  
> O provedor MAPI não suporta o cliente MAPI para rápida desligamento.
    
## <a name="remarks"></a>Coment�rios

Provedores MAPI que não é necessário para suportar o desligamento rápido do cliente ainda devem implementar a interface [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) e têm o método **IMAPIProviderShutdown::QueryFastShutdown** retornar MAPI_E_NO_SUPPORT. Para o Outlook como um cliente MAPI, isso faz com que o Outlook esperar por todas as referências externas ser liberada antes de sair. 
  
Dependendo do registro do Windows do usuário configuração para fast desligamento, não Implementando a interface de **IMAPIProviderShutdown** não necessariamente impede que um desligamento rápido de cliente. 
  
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


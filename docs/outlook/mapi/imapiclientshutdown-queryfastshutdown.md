---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584930"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O subsistema MAPI para desligamento rápido de consultas suporte que é fornecido por provedores MAPI carregados.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor retornado

S_OK
  
> O subsistema de MAPI suporta o cliente MAPI para rápida desligamento.
    
MAPI_E_NO_SUPPORT
  
> O provedor MAPI não suporta o cliente MAPI para rápida desligamento.
    
## <a name="remarks"></a>Comentários

Se o subsistema de MAPI suporta o cliente MAPI rápida desligamento depende da configuração de registro do Windows do usuário ou o comportamento padrão do cliente MAPI para desligamento rápido. Ele também depende da capacidade dos provedores MAPI carregados para suportar o desligamento rápido. Para obter mais informações, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


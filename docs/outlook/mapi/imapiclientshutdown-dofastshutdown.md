---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408681"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica a intenção de que o cliente MAPI saia imediatamente do processo do cliente.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O subsistema MAPI indicou que carregou provedores MAPI que o cliente MAPI está saindo imediatamente e os provedores MAPI estão prontos para a saída do cliente.
    
MAPI_E_NO_SUPPORT
  
> O subsistema MAPI não dá suporte a desligamento rápido do cliente.
    
## <a name="remarks"></a>Comentários

Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::D ofastshutdown** com base no resultado de S_OK RETORNADO pelo subsistema MAPI no o método [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obter mais informações, consulte [práticas recomendadas para](best-practices-for-fast-shutdown.md)o desligamento rápido.
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


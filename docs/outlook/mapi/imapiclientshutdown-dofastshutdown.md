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
  
Indica a intenção do cliente MAPI de sair do processo de cliente imediatamente.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O subsistema de MAPI indicou para os provedores de MAPI carregados que o cliente MAPI está saindo imediatamente, e os provedores de MAPI estão prontos para a saída do cliente.
    
MAPI_E_NO_SUPPORT
  
> O subsistema MAPI não dá suporte ao desligamento rápido do cliente.
    
## <a name="remarks"></a>Comentários

Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::D oFastShutdown** com base no resultado S_OK retornado pelo subsistema de MAPI no método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Para obter mais informações, consulte [As Práticas Recomendadas para o Desligamento Rápido.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


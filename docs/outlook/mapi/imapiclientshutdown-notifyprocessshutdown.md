---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438866"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica a intenção do cliente MAPI de prosseguir com o desligado.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O subsistema de MAPI tentou notificar os provedores MAPI carregados de que o cliente MAPI fará um desligamento rápido.
    
## <a name="remarks"></a>Comentários

Para evitar a perda de dados do desligamento rápido de um cliente MAPI, os clientes MAPI devem chamar os métodos **IMAPIClientShutdown::NotifyProcessShutdown** e [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) com base no resultado S_OK retornado pelo subsistema de MAPI no método [IMAPIClientShutdown::QueryFastShutdown.](imapiclientshutdown-queryfastshutdown.md) Para obter mais informações, consulte [As Práticas Recomendadas para o Desligamento Rápido.](best-practices-for-fast-shutdown.md)
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


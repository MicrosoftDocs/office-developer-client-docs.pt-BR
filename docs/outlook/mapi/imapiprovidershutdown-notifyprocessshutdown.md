---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326387"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica ao provedor MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa realizar ações para evitar a perda de dados.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O provedor MAPI está executando ações para evitar a perda de dados quando o cliente MAPI é desligado.
    
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


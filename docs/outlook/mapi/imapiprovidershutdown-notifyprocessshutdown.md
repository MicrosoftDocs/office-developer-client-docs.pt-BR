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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cce98dc630dd9f7fa459ca31d94d012ba9a7fd85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767167"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a>IMAPIProviderShutdown::NotifyProcessShutdown

  
  
**Aplica-se a**: Outlook 
  
Indica o provedor MAPI que um cliente MAPI irá fazer um rápido desligamento, para que o provedor pode executar ações para evitar a perda de dados.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor retornado

S_OK
  
> O provedor MAPI está demorando ações para evitar a perda de dados quando o cliente MAPI desligado.
    
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown: IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


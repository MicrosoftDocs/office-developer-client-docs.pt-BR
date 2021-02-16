---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428841"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica ao provedor de MAPI que o cliente MAPI está saindo imediatamente, para que o provedor de MAPI persista alterações para evitar a perda de dados.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O provedor MAPI está pronto para que o cliente MAPI saia imediatamente. 
    
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


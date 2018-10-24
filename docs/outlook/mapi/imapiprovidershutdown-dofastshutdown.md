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
ms.openlocfilehash: faa061ae323dd744d12e4f9abec713c71379feba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563468"
---
# <a name="imapiprovidershutdowndofastshutdown"></a>IMAPIProviderShutdown::DoFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o provedor MAPI que o cliente MAPI está deixando imediatamente, para que o provedor MAPI persistirá alterações para evitar a perda de dados.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O provedor MAPI está pronto para o cliente MAPI sair imediatamente. 
    
## <a name="see-also"></a>Confira também



[IMAPIProviderShutdown : IUnknown](imapiprovidershutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


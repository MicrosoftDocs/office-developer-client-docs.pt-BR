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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 447832d88a9740875fcf39a32adcf4ebb99e05ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766936"
---
# <a name="imapiclientshutdowndofastshutdown"></a>IMAPIClientShutdown::DoFastShutdown

  
  
**Aplica-se a**: Outlook 
  
Indica a intenção do cliente MAPI para sair do processo de cliente imediatamente.
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a>Valor retornado

S_OK
  
> O subsistema de MAPI tenha indicado para provedores MAPI carregados que o cliente MAPI está deixando imediatamente e os provedores MAPI estão prontos para sair do cliente.
    
MAPI_E_NO_SUPPORT
  
> O subsistema de MAPI não suporta o desligamento rápido do cliente.
    
## <a name="remarks"></a>Coment�rios

Para evitar a perda de dados do fast desligamento de um cliente MAPI, clientes MAPI devem chamar os métodos [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) e **IMAPIClientShutdown::DoFastShutdown** com base no resultado S_OK retornado pelo subsistema de MAPI em o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obter mais informações, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


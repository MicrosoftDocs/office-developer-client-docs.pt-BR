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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 04a9b631c3a4f33282bce44e06d92e089349c76b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766930"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a>IMAPIClientShutdown::NotifyProcessShutdown

  
  
**Aplica-se a**: Outlook 
  
Indica a intenção do cliente MAPI para prosseguir com desligado.
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a>Valor retornado

S_OK
  
> O subsistema de MAPI tentou notificar carregados provedores MAPI que o cliente MAPI irá fazer um desligamento rápido.
    
## <a name="remarks"></a>Coment�rios

Para evitar a perda de dados do fast desligamento de um cliente MAPI, clientes MAPI devem chamar os métodos **IMAPIClientShutdown::NotifyProcessShutdown** e [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) com base no resultado S_OK retornado pelo subsistema de MAPI em o método [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) . Para obter mais informações, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown: IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


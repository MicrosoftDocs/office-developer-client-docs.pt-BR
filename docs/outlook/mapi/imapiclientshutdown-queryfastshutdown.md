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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418145"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a>IMAPIClientShutdown::QueryFastShutdown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Consulta o subsistema MAPI para obter suporte de desligamento rápido fornecido por provedores MAPI carregados.
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a>Valor de retorno

S_OK
  
> O subsistema MAPI oferece suporte ao cliente MAPI para fazer desligamento rápido.
    
MAPI_E_NO_SUPPORT
  
> O provedor MAPI não dá suporte ao cliente MAPI para fazer desligamento rápido.
    
## <a name="remarks"></a>Comentários

Se o subsistema MAPI suporta o cliente MAPI para fazer o desligamento rápido depende da configuração do registro do Windows do usuário ou o comportamento padrão do cliente MAPI para o desligamento rápido. Também depende da capacidade dos provedores MAPI carregados suportar o desligamento rápido. Para obter mais informações, consulte [Opções de usuário](fast-shutdown-user-options.md)de desligamento rápido.
  
## <a name="see-also"></a>Confira também



[IMAPIClientShutdown : IUnknown](imapiclientshutdowniunknown.md)


[Desligamento do cliente em MAPI](client-shutdown-in-mapi.md)


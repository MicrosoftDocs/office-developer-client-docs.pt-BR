---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434141"
---
# <a name="upreade"></a>UPREADE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações estendidas para carregar o estado de leitura de um item durante o [estado de status de leitura do upload.](upload-read-status-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Membros

_ulFlags_
  
>  [out]/[in] Sinalizadores para determinar o comportamento apropriado durante o upload. 
    
  - UPR_ASSOC
    
    - [out] O item está oculto.
    
  - UPR_READ
    
    - [out] O status de leitura do item foi alterado.
    
  - UPR_OK
    
    - [in] O carregamento foi bem-sucedido. O cliente define isso depois de carregar informações no servidor.
    
  - UPR_COMMIT
    
    - [in] Carregue o status de leitura do item agora, [](upload-table-state.md) em vez de aguardar até o final do estado da tabela de carregamento para processar em lote mais de um item. 
    
_skey_
  
> [out] Chave de origem do item.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes de MAPI](mapi-constants.md)
- [UPREAD](upread.md)


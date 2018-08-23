---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579071"
---
# <a name="upreade"></a>UPREADE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações estendidas para carregar o estado de leitura de um item durante o [carregamento ler o estado de status](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
>  [out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento. 
    
  - UPR_ASSOC
    
    - [out] Item é oculto.
    
  - UPR_READ
    
    - [out] O status de leitura do item foi alterado.
    
  - UPR_OK
    
    - [in] Carregamento foi bem-sucedida. O cliente define esta após carregar as informações para o servidor.
    
  - UPR_COMMIT
    
    - [in] Carrega o status de leitura do item agora, em vez de aguardar até o final da [carregar o estado de tabela](upload-table-state.md) para processamento em lotes mais de um item. 
    
_skey_
  
> [out] Chave de origem do item.
    
## <a name="see-also"></a>Confira também

- [Sobre a API de replicação](about-the-replication-api.md)
- [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [UPREAD](upread.md)


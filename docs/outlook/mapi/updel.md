---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581122"
---
# <a name="updel"></a>UPDEL

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para itens que foram excluídos em um repositório local. Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupde_
  
>  [out] Vetor de [UPDELE](updele.md) entradas. 
    
 _cEnt_
  
> [out] Número de entradas em *pupde* . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)


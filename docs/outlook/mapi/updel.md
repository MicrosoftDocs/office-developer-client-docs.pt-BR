---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770663"
---
# <a name="updel"></a>UPDEL

  
  
**Aplica-se a**: Outlook 
  
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
  
[Constantes MAPI](mapi-constants.md)


---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770680"
---
# <a name="upread"></a>UPREAD

  
  
**Aplica-se a**: Outlook 
  
Informações para carregar o estado de leitura dos itens durante o [carregamento ler o estado de status](upload-read-status-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupre_
  
>  [out] Vetor de **[UPREADE](upreade.md)** entradas. 
    
 _cEnt_
  
>  [out] Número de entradas **UPREADE** . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)


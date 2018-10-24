---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 887c66277b54e2e14c7f67c76b8e9dd4fa8bc719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589228"
---
# <a name="upread"></a>UPREAD

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
[Constantes de MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)


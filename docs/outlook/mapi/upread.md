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
ms.openlocfilehash: 7338edc13227e303ec5fa47da4a5d9ee611c6749
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419881"
---
# <a name="upread"></a>UPREAD

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para carregar o estado de leitura dos itens durante o [estado de status de leitura do upload.](upload-read-status-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membros

 _pupre_
  
>  [out] Vetor de **[entradas UPREADE.](upreade.md)** 
    
 _cEnt_
  
>  [out] Número de **entradas UPREADE.** 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)
  
[UPREADE](upreade.md)


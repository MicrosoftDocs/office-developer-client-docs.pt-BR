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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436794"
---
# <a name="updel"></a>UPDEL

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para itens que foram excluídos em um armazenamento local. Essas informações são usadas durante o [estado de status de exclusão de upload.](upload-delete-status-state.md)
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membros

 _atade_
  
>  [out] Vetor de [entradas UPDELE.](updele.md) 
    
 _cEnt_
  
> [out] Número de entradas em  *velde*  . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)


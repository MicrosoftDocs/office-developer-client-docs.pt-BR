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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360484"
---
# <a name="updel"></a>UPDEL

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Informações para itens que foram excluídos em um repositório local. Essas informações são usadas durante o [estado de status de exclusão de upload](upload-delete-status-state.md).
  
## <a name="quick-info"></a>Informações rápidas

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Membros

 _pupde_
  
>  bota Vetor de entradas de [UPDELE](updele.md) . 
    
 _cEnt_
  
> bota Número de entradas no *pupde* . 
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[Constantes de MAPI](mapi-constants.md)


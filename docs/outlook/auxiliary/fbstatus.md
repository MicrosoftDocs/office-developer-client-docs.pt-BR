---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Uma enumeração para o status de livre/ocupado dos blocos de livre/ocupado.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424088"
---
# <a name="fbstatus"></a>FBStatus

Uma enumeração para o status de livre/ocupado dos blocos de livre/ocupado.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a>Comentários

O status de livre/ocupado de um bloco de tempo determina como ele é exibido em um **calendário:** **Livre,** Ocupado **,** Provisório ou Fora **do Escritório.** 
  
## <a name="see-also"></a>Confira também

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)


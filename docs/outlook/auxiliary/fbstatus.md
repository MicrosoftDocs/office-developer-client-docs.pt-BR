---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Uma enumeração para o status livre/ocupado de blocos de livre/ocupado.
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765808"
---
# <a name="fbstatus"></a>FBStatus

Uma enumeração para o status livre/ocupado de blocos de livre/ocupado.
  
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

## <a name="remarks"></a>Coment�rios

O status livre/ocupado de um bloco de tempo determina como ele é exibido em um calendário: **disponível**, **ocupado**, **Provisório**ou **Ausência temporária**. 
  
## <a name="see-also"></a>Confira também

- [FBBlock_1](fbblock_1.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)


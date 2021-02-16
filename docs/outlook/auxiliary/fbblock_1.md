---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define um bloco de dados de livre/ocupado. Este é um item em um calendário representado por um compromisso ou solicitação de reunião.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413196"
---
# <a name="fbblock_1"></a>FBBlock_1

Define um bloco de dados de livre/ocupado. Este é um item em um calendário representado por um compromisso ou uma solicitação de reunião.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a>Membros

_m_tmStart_
  
> A hora de início do bloco, expressa em tempo relativo. Para obter mais informações, [consulte Usar o tempo relativo para acessar dados de livre/ocupado.](how-to-use-relative-time-to-access-free-busy-data.md)
    
_m_tmEnd_
  
> A hora de término do bloco, expressa em tempo relativo.
    
_m_fbStatus_
  
> O status de livre/ocupado para esse bloco, indicando se o usuário está fora do escritório,  ocupado, provisório ou livre, durante o período de tempo entre m_tmStart e _m_tmEnd_.
    
## <a name="see-also"></a>Confira também

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Usar o tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md)


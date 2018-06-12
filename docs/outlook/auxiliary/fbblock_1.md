---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define um bloco de informações de disponibilidade de dados. Este é um item em um calendário representado por uma solicitação de reunião ou compromisso.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765797"
---
# <a name="fbblock1"></a>FBBlock_1

Define um bloco de informações de disponibilidade de dados. Este é um item em um calendário representado por uma solicitação de reunião ou compromisso.
  
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
  
> A hora de início para o bloco, expresso em tempo relativo. Para obter mais informações, consulte [tempo relativo para acessar informações de disponibilidade de dados de uso](how-to-use-relative-time-to-access-free-busy-data.md).
    
_m_tmEnd_
  
> A hora de término para o bloco, expresso em tempo relativo.
    
_m_fbStatus_
  
> O status livre/ocupado para este bloco, que indica se o usuário está fora do escritório, ocupado, provisório ou livre, durante o período de tempo entre _m_tmStart_ e _m_tmEnd_.
    
## <a name="see-also"></a>Confira também

- [FBStatus](fbstatus.md)
- [IEnumFBBlock::Next](ienumfbblock-next.md)
- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)


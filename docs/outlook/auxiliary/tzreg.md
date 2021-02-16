---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define quando o horário de verão é iniciado, quando ocorre o retorno ao horário padrão e quantas horas é o horário de verão.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419363"
---
# <a name="tzreg"></a>TZREG

Define quando o horário de verão é iniciado, quando ocorre o retorno ao horário padrão e quantas horas é o horário de verão.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Membros

_lBias_
  
> O deslocamento do horário de Greenwich (GMT).
    
_lStandardBias_
  
> O deslocamento do bias durante a hora padrão.
    
_lDaylightBias_
  
> O deslocamento do bias durante o horário de verão.
    
_stStandardDate_
  
> O tempo para alternar para a hora padrão.
    
_stDaylightDate_
  
> A hora de alternar para o horário de verão.
    
## <a name="remarks"></a>Comentários

Essa estrutura é semelhante a **TIME_ZONE_INFORMATION**. Essa é a estrutura usada por clientes herdados para armazenar informações de fuso horário para reuniões recorrentes.
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)


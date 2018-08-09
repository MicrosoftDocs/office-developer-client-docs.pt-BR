---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define quando inicia o horário de verão, quando o retorno para a hora padrão ocorre e é de horário de verão shift quantas horas.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766086"
---
# <a name="tzreg"></a>TZREG

Define quando inicia o horário de verão, quando o retorno para a hora padrão ocorre e é de horário de verão shift quantas horas.
  
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

## <a name="members"></a>Members

_lBias_
  
> O deslocamento de hora de Greenwich (GMT).
    
_lStandardBias_
  
> O deslocamento de bias durante a hora padrão.
    
_lDaylightBias_
  
> O deslocamento de bias durante o horário de verão.
    
_stStandardDate_
  
> O tempo para alternar para a hora padrão.
    
_stDaylightDate_
  
> O tempo para alternar para o horário de verão.
    
## <a name="remarks"></a>Comentários

Essa estrutura é semelhante ao **TIME_ZONE_INFORMATION**. Esta é a estrutura usada por clientes herdados para armazenar informações de fuso horário para reuniões recorrentes.
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)


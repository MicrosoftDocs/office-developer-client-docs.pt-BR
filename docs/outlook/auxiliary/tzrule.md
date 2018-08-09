---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica as informações de uma regra de fuso horário sobre quando inicia o horário de verão e o ano em que essa regra de fuso horário primeiro entrará em vigor.
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766084"
---
# <a name="tzrule"></a>TZRULE

Especifica as informações de uma regra de fuso horário sobre quando inicia o horário de verão e o ano em que essa regra de fuso horário primeiro entrará em vigor. 
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Members

_wFlags_
  
> Os sinalizadores definidos para este membro identificam detalhes específicos para essa regra de fuso horário. Os sinalizadores possíveis são:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** — identifica a regra como aquele que deve ser usada no momento. Somente uma regra pode ser marcada como a regra efetiva. Todas as outras regras são apenas para fins de comparação. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** — em reuniões recorrentes, identifica a regra como correspondência da regra na [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Isso pode ser usado para detectar se **PidLidTimeZoneStruct** tiver sido modificada significativamente por um cliente herdado, qual seria caso contrário, não sabem da propriedade nova e mais completa. 
    
_stStart_
  
> A hora no tempo Universal Coordenado (UTC) que a regra de fuso horário é iniciada.
    
_TZReg_
  
> As informações de fuso horário para a regra de fuso horário.
    
## <a name="remarks"></a>Comentários

Essa estrutura aumenta [TZREG](tzreg.md) fornecendo informações adicionais indicando quando as regras de fuso horário entrem em vigor. 
  
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)


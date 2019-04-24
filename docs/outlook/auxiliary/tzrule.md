---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica as informações de uma regra de fuso horário sobre quando começa o horário de verão e o ano em que essa regra de fuso horário entrou em vigor.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328613"
---
# <a name="tzrule"></a>TZRULE

Especifica as informações de uma regra de fuso horário sobre quando começa o horário de verão e o ano em que essa regra de fuso horário entrou em vigor. 
  
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
  
> Os sinalizadores definidos para esse membro identificam os detalhes específicos da regra de fuso horário. Os sinalizadores possíveis são os seguintes:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG**: identifica a regra que deve ser usada no momento. Somente uma regra pode ser marcada como a regra efetiva. Todas as regras são apenas para fins de comparação. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG**: em reuniões recorrentes, identifica a regra como correspondente à regra em [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Pode ser usado para detectar se **PidLidTimeZoneStruct** foi modificado significativamente por um cliente herdado, o que, caso contrário, passaria despercebido pelo nova propriedade mais completa. 
    
_stStart_
  
> A hora em UTC (Tempo Universal Coordenado) que a regra de fuso horário iniciou.
    
_TZReg_
  
> As informações de fuso horário para a regra de fuso horário.
    
## <a name="remarks"></a>Comentários

Essa estrutura aumenta [TZREG](tzreg.md) fornecendo informações adicionais que indicam quando as regras de fuso horário entram em vigor. 
  
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Constantes (APIs exportadas pelo Outlook)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)


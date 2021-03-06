---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa um fuso horário inteiro, incluindo todas as regras de turno de fuso horário histórico, atual e futuro para o horário de verão.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429338"
---
# <a name="tzdefinition"></a>TZDEFINITION

Representa um fuso horário inteiro, incluindo todas as regras de turno de fuso horário histórico, atual e futuro para o horário de verão.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Members

_wFlags_
  
> Indica que o nome da chave que representa o fuso horário no Registro do Windows é válido. Como cada fuso horário deve ser sempre identificado por um nome de chave, esse membro sempre deve ter o valor **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> O nome da chave para este fuso horário no Registro do Windows. Esse nome não deve ser localizado. Ele tem um tamanho máximo de **MAX_PATH**, que é definido no arquivo de header windows.h do Software Development Kit do Windows (SDK do Windows). 
    
_cRules_
  
> O número de regras de fuso horário para esta definição. O número máximo de regras é **TZ_MAX_RULES**. 
    
_rgRules_
  
> Uma matriz de regras que descrevem quando ocorrem turnos.
    
## <a name="remarks"></a>Comentários

Deve haver pelo menos uma regra em  *rgRules*  . A primeira regra em  *rgRules*  é considerada a regra a ser usada até que a segunda regra seja iniciada, independentemente do  *stStart*  na primeira regra. 
  
As regras devem ser ordenadas da mais antiga para a mais recente. Não há sobreposição permitida entre as regras, portanto, uma regra anterior é considerada para terminar quando uma nova regra é iniciada.
  
## <a name="see-also"></a>Confira também

- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)


---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa um fuso horário inteiro, incluindo todas as regras de shift históricas, atuais e futuros de fuso horário de verão.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766096"
---
# <a name="tzdefinition"></a>TZDEFINITION

Representa um fuso horário inteiro, incluindo todas as regras de shift históricas, atuais e futuros de fuso horário de verão.
  
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
  
> Indica que o nome da chave que representa o fuso horário no registro do Windows é válido. Como cada fuso horário sempre deve ser identificado por um nome de chave, esse membro sempre deve ter o valor **TZDEFINITION_FLAG_VALID_KEYNAME**.
    
_pwszKeyName_
  
> O nome da chave para este fuso horário no registro do Windows. Esse nome não deve estar localizado. Ele tem um tamanho máximo de **MAX_PATH**, que é definida no Windows. arquivo de cabeçalho do Software Development Kit (SDK) do Windows h. 
    
_cRules_
  
> O número de regras para esta definição de fuso horário. O número máximo de regras é **TZ_MAX_RULES**. 
    
_rgRules_
  
> Uma matriz de regras que descrevem quando desloca ocorre.
    
## <a name="remarks"></a>Comentários

Deve haver pelo menos uma regra *rgRules* . A primeira regra no *rgRules* é considerado a regra usar até a segunda regra for iniciado, independentemente do *stStart* na primeira regra. 
  
As regras devem ser classificadas do mais antigo para o mais recente. Não há nenhuma sobreposição permitida entre as regras, portanto, uma regra anterior é considerada para encerrar quando inicia uma nova regra.
  
## <a name="see-also"></a>Confira também

- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)


---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770504"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Aplica-se a**: Outlook 
  
Descreve uma restrição de tamanho para o qual é utilizada para testar o tamanho de um valor de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a>Members

 **RelOp**
  
> Operador relacional que é usada na comparação tamanho. Os valores possíveis são: 
    
RELOP_GE 
  
> A comparação é feita com base no primeiro um valor maior ou igual.
    
RELOP_GT 
  
> A comparação é feita com base em um valor maior de primeiro.
    
RELOP_LE 
  
> A comparação é feita com base no primeiro um valor menor ou igual.
    
RELOP_LT 
  
> A comparação é feita com base em um valor menor de primeiro.
    
RELOP_NE 
  
> A comparação é feita com base nos valores desiguais.
    
RELOP_RE 
  
> A comparação é feita com base em como valores (expressão regular).
    
RELOP_EQ 
  
> A comparação é feita com base nos valores iguais.
    
 **ulPropTag**
  
> Marca de propriedade que identifica a propriedade a ser testado.
    
 **cb**
  
> Contagem de bytes no valor da propriedade.
    
## <a name="remarks"></a>Comentários

Para obter uma discussão geral de como funcionam os restrições, consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


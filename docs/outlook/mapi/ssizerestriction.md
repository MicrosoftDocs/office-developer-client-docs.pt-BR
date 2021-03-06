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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439083"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de tamanho que é usada para testar o tamanho de um valor de propriedade. 
  
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

 **re ltda**
  
> Operador relacional que é usado na comparação de tamanho. Os valores possíveis são: 
    
RELOP_GE 
  
> A comparação é feita com base em um primeiro valor maior ou igual.
    
RELOP_GT 
  
> A comparação é feita com base em um primeiro valor maior.
    
RELOP_LE 
  
> A comparação é feita com base em um primeiro valor menor ou igual.
    
RELOP_LT 
  
> A comparação é feita com base em um primeiro valor menor.
    
RELOP_NE 
  
> A comparação é feita com base em valores de valores de valores diferentes.
    
RELOP_RE 
  
> A comparação é feita com base nos valores LIKE (expressão regular).
    
RELOP_EQ 
  
> A comparação é feita com base em valores iguais.
    
 **ulPropTag**
  
> Marca de propriedade que identifica a propriedade a ser testado.
    
 **cb**
  
> Contagem de bytes no valor da propriedade.
    
## <a name="remarks"></a>Comentários

Para uma discussão geral sobre como funcionam as restrições, consulte [Sobre restrições.](about-restrictions.md) 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


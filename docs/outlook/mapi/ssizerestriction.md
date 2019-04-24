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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344475"
---
# <a name="ssizerestriction"></a>SSizeRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de tamanho que é usada para testar o tamanho de um valor de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Operador relacional usado na comparação de tamanho. Os valores possíveis são os seguintes: 
    
RELOP_GE 
  
> A comparação é feita com base em um valor maior ou igual a um primeiro.
    
RELOP_GT 
  
> A comparação é feita com base em um primeiro valor maior.
    
RELOP_LE 
  
> A comparação é feita com base em um valor menor ou igual a.
    
RELOP_LT 
  
> A comparação é feita com base em um primeiro valor menor.
    
RELOP_NE 
  
> A comparação é feita com base em valores desiguais.
    
RELOP_RE 
  
> A comparação é feita com base nos valores LIKE (expressão regular).
    
RELOP_EQ 
  
> A comparação é feita com base em valores iguais.
    
 **ulPropTag**
  
> Marca de propriedade identificando a propriedade a ser testada.
    
 **cb**
  
> Contagem de bytes no valor da propriedade.
    
## <a name="remarks"></a>Comentários

Para uma discussão geral de como as restrições funcionam, consulte [about Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


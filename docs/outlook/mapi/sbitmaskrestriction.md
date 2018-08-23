---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9197201388530bd7755eb1987ecc863220e3847
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566604"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de bitmask, que é usada para realizar uma operação de **AND** bit a bit e o resultado do teste. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a>Members

 **relBMR**
  
> Operador relacional que descreve como a máscara especificada no membro **ulMask** deve ser aplicada a marca de propriedade. Os valores possíveis são: 
    
BMR_EQZ 
  
> Execute uma operação **AND** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste de como sendo igual a zero. 
    
BMR_NEZ 
  
> Execute uma operação **AND** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para não sendo igual a zero. 
    
 **ulPropTag**
  
> Propriedade marca da propriedade à qual o bitmask é aplicado.
    
 **ulMask**
  
> Bitmask a ser aplicado à propriedade identificada pela **ulPropTag**.
    
## <a name="remarks"></a>Comentários

A estrutura **SBitMaskRestriction** executa uma operação **AND** bit a bit, usando o bitmask descrito no membro **ulMask** e o valor da propriedade descrito pelo membro **ulPropTag** . Se o resultado for zero, BMR_EQZ será satisfeita. Se for diferente de zero, ou seja, se o valor da propriedade tenha pelo menos uma dos mesmos bits definido como **ulMask**, em seguida, BMR_NEZ será satisfeita.
  
Para obter mais informações sobre a estrutura de **SBitMaskRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


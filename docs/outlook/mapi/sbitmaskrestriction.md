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
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424473"
---
# <a name="sbitmaskrestriction"></a>SBitMaskRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de bitmask, que é usada para executar uma operação **e** bits e testar o resultado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Operador relacional que descreve como a máscara especificada no membro **ulMask** deve ser aplicada à marca da propriedade. Os valores possíveis são os seguintes: 
    
BMR_EQZ 
  
> Execute uma operação **e** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para ser igual a zero. 
    
BMR_NEZ 
  
> Execute uma operação **e** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para não ser igual a zero. 
    
 **ulPropTag**
  
> Marca de propriedade da propriedade à qual a bitmask é aplicada.
    
 **ulMask**
  
> Bitmask a ser aplicado à propriedade identificada por **ulPropTag**.
    
## <a name="remarks"></a>Comentários

A estrutura **SBitMaskRestriction** executa uma operação **e** bit a bit usando a bitmask descrita no membro **ulMask** e o valor da propriedade descrita pelo membro **ulPropTag** . Se o resultado for zero, BMR_EQZ será satisfeito. Se for diferente de zero, ou seja, se o valor da propriedade tiver pelo menos um dos mesmos bits definido como **ulMask**, então BMR_NEZ será satisfeito.
  
Para obter mais informações sobre a estrutura e as restrições do **SBitMaskRestriction** em geral, consulte [about Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


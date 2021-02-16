---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418936"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição existente que é usada para testar se uma determinada propriedade existe como uma coluna na tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Reservado; deve ser zero. 
    
 **ulPropTag**
  
> Marca de propriedade que identifica a coluna a ser testada quanto à existência em cada linha.
    
 **ulReserved2**
  
> Reservado; deve ser zero.
    
## <a name="remarks"></a>Comentários

A restrição existente é usada para garantir resultados significativos para outros tipos de restrições que envolvem propriedades, como restrições de propriedade e conteúdo. Quando uma restrição que envolve uma propriedade é passada para [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) e a propriedade não existe, os resultados da restrição são indefinido. Ao criar uma **restrição AND** que une a restrição de propriedade com uma restrição existente, um chamador pode ter resultados precisos garantidos. 
  
Restrições existentes não podem ser usadas com propriedades de subpro object que tenham o tipo PT_OBJECT. 
  
Para obter mais informações sobre a **estrutura SExistRestriction,** consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


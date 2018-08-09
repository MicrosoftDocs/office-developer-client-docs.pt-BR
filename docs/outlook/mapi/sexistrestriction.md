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
ms.openlocfilehash: 62b5a42a540a4fb96761c45cd51c510f12225e9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770393"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**Aplica-se a**: Outlook 
  
Descreve uma restrição existem que é usada para testar se uma determinada propriedade existe como uma coluna da tabela. 
  
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
  
> Marca de propriedade que identifica a coluna a ser testado existência em cada linha.
    
 **ulReserved2**
  
> Reservado; deve ser zero.
    
## <a name="remarks"></a>Comentários

A restrição da lista é usada para garantir resultados significativos para outros tipos de restrições que envolvem propriedades, como restrições de propriedade e conteúdo. Quando uma restrição que envolva uma propriedade é passada para [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) e a propriedade não existir, os resultados da restrição são indefinidos. Criando uma restrição **e** que une a restrição de propriedade com uma restrição existem, um chamador pode ser garantido resultados exatos. 
  
Existem restrições não podem ser usadas com propriedades do objeto sub-recurso que têm tipo PT_OBJECT. 
  
Para obter mais informações sobre a estrutura **SExistRestriction** , consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


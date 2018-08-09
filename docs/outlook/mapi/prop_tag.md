---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e53c39b713aa782eb387b85667f5ded6193006f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770174"
---
# <a name="proptag"></a>PROP_TAG

**Aplica-se a**: Outlook 
  
Retorna uma marca de propriedade criada pela combinação de um tipo de propriedade especificado e o identificador. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |[SPropValue](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a>Parâmetros

_ulPropType_
  
> Tipo de propriedade para a nova marca de propriedade.
    
_ulPropID_
  
> Identificador de propriedade para a nova marca de propriedade.
    
## <a name="remarks"></a>Comentários

O **PROP\_marca** macro cria uma marca de propriedade para uma propriedade do tipo _ulPropType_ e o identificador especificado em _ulPropID_. Por exemplo, uma marca de propriedade para um identificador de entrada pode ser criada usando a macro **PROP_TAG** da seguinte maneira: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Os 16 bits de ordem baixa da marca de propriedade retornados contêm o tipo da propriedade PT_BINARY, e as ordem alta 16 bits contêm o identificador de propriedade, 0xFFFF.
  
Para obter mais informações sobre marcas de propriedade, consulte [Marcas de propriedade de MAPI](mapi-property-tags.md).
  
## <a name="see-also"></a>Confira também

- [SPropValue](spropvalue.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


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
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425880"
---
# <a name="prop_tag"></a>PROP_TAG

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma marca de propriedade criada combinando um tipo de propriedade e um identificador especificados. 
  
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

A macro **\_ PROP TAG** cria uma marca de propriedade para uma propriedade do tipo  _ulPropType_ e o identificador especificado em  _ulPropID_. Por exemplo, uma marca de propriedade para um identificador de entrada pode ser criada usando PROP_TAG **macro** da seguinte forma: 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

Os 16 bits de ordem baixa da marca de propriedade retornada contêm o tipo de propriedade, PT_BINARY e os 16 bits de alta ordem contêm o identificador de propriedade, 0xFFFF.
  
Para obter mais informações sobre marcas de propriedade, consulte [MARCAS de propriedade MAPI.](mapi-property-tags.md)
  
## <a name="see-also"></a>Confira também

- [SPropValue](spropvalue.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


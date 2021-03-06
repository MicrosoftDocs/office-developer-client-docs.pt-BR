---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f873ad5234460f9f1781c7427b60d285f7486196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429345"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [SPropTagArray](sproptagarray.md) nomeada que inclui um número especificado de marcas de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parâmetros

_ _ctag_
  
> Contagem de marcas de propriedade a serem incluídas na nova estrutura.
    
_ _name_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSPropTagArray** para criar uma matriz de marca de propriedade com limites explícitos. 
  
Para usar a nova estrutura que resulta da macro **SizedSPropTagArray** como um ponteiro para uma **estrutura SPropTagArray,** execute a seguinte projeção: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Confira também

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282695"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada [SPropTagArray](sproptagarray.md) que inclui um número especificado de marcas de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parâmetros

__CTAG_
  
> Contagem de marcas de propriedade a serem incluídas na nova estrutura.
    
__nome_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSPropTagArray** para criar uma matriz de marca de propriedade com os limites explícitos. 
  
Para usar a nova estrutura que resulta da macro **SizedSPropTagArray** como um ponteiro para uma estrutura **SPropTagArray** , execute a seguinte conversão: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Confira também

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


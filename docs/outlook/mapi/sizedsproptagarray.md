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
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573618"
---
# <a name="sizedsproptagarray"></a>SizedSPropTagArray

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [SPropTagArray](sproptagarray.md) nomeada que inclua um número especificado de marcas de propriedade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SPropTagArray** <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a>Parâmetros

__ctag_
  
> Contagem de marcas de propriedade a ser incluído na nova estrutura.
    
__nome_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSPropTagArray** para criar uma matriz de marca de propriedade com limites explícitos. 
  
Para usar a nova estrutura que é resultado da macro **SizedSPropTagArray** como um ponteiro para uma estrutura **SPropTagArray** , execute a seguinte projeção: 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a>Confira também

- [SPropTagArray](sproptagarray.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


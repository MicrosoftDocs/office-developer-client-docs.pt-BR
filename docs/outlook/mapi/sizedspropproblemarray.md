---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594611"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [SPropProblemArray](spropproblemarray.md) nomeada que contém um número especificado de estruturas de [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parâmetros

__cprob_
  
> Contagem de estruturas de **SPropProblem** a serem incluídos na nova estrutura. 
    
__nome_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSPropProblemArray** para criar uma matriz de problema de propriedade com limites explícitos. Para usar a nova estrutura que é resultado da macro **SizedSPropProblemArray** como um ponteiro para uma estrutura **SPropProblemArray** , execute a seguinte projeção: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Confira também

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


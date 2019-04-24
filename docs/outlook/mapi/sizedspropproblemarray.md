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
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282688"
---
# <a name="sizedspropproblemarray"></a>SizedSPropProblemArray

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada do [SPropProblemArray](spropproblemarray.md) que contém um número especificado de estruturas [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**SPropProblemArray** <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a>Parâmetros

__cprob_
  
> Contagem de estruturas **SPropProblem** a serem incluídas na nova estrutura. 
    
__nome_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSPropProblemArray** para criar uma matriz com problema de propriedade com os limites explícitos. Para usar a nova estrutura que resulta da macro **SizedSPropProblemArray** como um ponteiro para uma estrutura **SPropProblemArray** , execute a seguinte conversão: 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a>Confira também

- [SPropProblemArray](spropproblemarray.md)
- [SPropProblem](spropproblem.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


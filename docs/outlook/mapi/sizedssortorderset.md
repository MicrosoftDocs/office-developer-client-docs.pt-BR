---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770437"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Aplica-se a**: Outlook 
  
Cria uma estrutura [SSortOrderSet](ssortorderset.md) nomeada que contém um número especificado de ordens de classificação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parâmetros

__csort_
  
> Contagem de ordens de classificação a ser incluído na nova estrutura.
    
__nome_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSSortOrderSet** para criar uma ordem de classificação definida com limites explícitos. 
  
Para usar a nova estrutura que é resultado da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet** , execute a seguinte projeção: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Confira também

- [SSortOrderSet](ssortorderset.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


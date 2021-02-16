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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428603"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura [SSortOrderSet](ssortorderset.md) nomeada que contém um número especificado de ordens de classificação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Parâmetros

_ _csort_
  
> Contagem de pedidos de classificação a serem incluídos na nova estrutura.
    
_ _name_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

Use a macro **SizedSSortOrderSet** para criar uma ordem de classificação definida com limites explícitos. 
  
Para usar a nova estrutura que resulta da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet,** execute a seguinte projeção: 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Confira também

- [SSortOrderSet](ssortorderset.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


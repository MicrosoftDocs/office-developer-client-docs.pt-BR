---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b7a93a9abb9a1c589ac7fdab3723c9c924eea0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770421"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Aplica-se a**: Outlook 
  
Cria uma estrutura [SRowSet](srowset.md) nomeada que contém um número especificado de linhas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Estrutura relacionada:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parâmetros

__galinha_
  
> Contagem do número de linhas a serem incluídos na nova estrutura.
    
__nome_
  
> Nome para a nova estrutura.
    
## <a name="remarks"></a>Comentários

Para usar a nova estrutura que é resultado da macro **SizedSRowSet** como um ponteiro para uma estrutura **SRowSet** , execute a seguinte projeção: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Confira também

- [SRowSet](srowset.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


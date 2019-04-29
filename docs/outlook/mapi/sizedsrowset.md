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
ms.openlocfilehash: cb1e19a3f3703dc4943a5f6c322f1c8b429da5fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410928"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma estrutura nomeada do [SRowSet](srowset.md) que contém um número especificado de linhas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Estrutura relacionada:  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Parâmetros

__galinha_
  
> Contagem do número de linhas a serem incluídas na nova estrutura.
    
__nome_
  
> Nome da nova estrutura.
    
## <a name="remarks"></a>Comentários

Para usar a nova estrutura que resulta da macro **SizedSRowSet** como um ponteiro para uma estrutura **SRowSet** , execute a seguinte conversão: 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Confira também

- [SRowSet](srowset.md)
- [Macros relacionadas a estruturas](macros-related-to-structures.md)


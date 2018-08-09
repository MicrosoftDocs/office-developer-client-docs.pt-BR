---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3fd61828cd631c4abc0131da867ca213a3c44d20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770489"
---
# <a name="spropproblemarray"></a>SPropProblemArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de uma ou mais estruturas de [SPropProblem](spropproblem.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSPropProblemArray](cbnewspropproblemarray.md) <br/> [CbSPropProblemArray](cbspropproblemarray.md) <br/> [SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a>Members

 **cProblem**
  
> Contagem de estruturas de [SPropProblem](spropproblem.md) na matriz indicado pelo membro **aProblem** . 
    
 **aProblem**
  
> Matriz de estruturas de **SPropProblem** , cada uma descrevendo um erro de propriedade. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre como as estruturas **SPropProblem** e **SPropProblemArray** funcionam com erros relacionados às propriedades, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md). 
  
## <a name="see-also"></a>Confira também



[SCODE](scode.md)
  
[SPropProblem](spropproblem.md)


[Estruturas MAPI](mapi-structures.md)


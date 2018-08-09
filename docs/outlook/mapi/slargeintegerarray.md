---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4d6785783f69857bd93f3c5818983e832e16af05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770443"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) que são usadas para descrever uma propriedade do tipo PT_MV_I8. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpli** . 
    
 **lpli**
  
> Ponteiro para uma matriz de estruturas **LARGE_INTEGER** reter os valores inteiros. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_18, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


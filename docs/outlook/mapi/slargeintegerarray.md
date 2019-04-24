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
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331385"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) que são usadas para descrever uma propriedade do tipo PT_MV_I8. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontada pelo membro **lpli** . 
    
 **lpli**
  
> Ponteiro para uma matriz de estruturas **LARGE_INTEGER** que contêm os valores inteiros. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre o PT_MV_18, confira [lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


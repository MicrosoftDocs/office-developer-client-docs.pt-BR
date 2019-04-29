---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406777"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores de tempo que são usados para descrever uma propriedade do tipo PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontada pelo membro **lpft** . 
    
 **lpft**
  
> Ponteiro para uma matriz de estruturas [FILETIME](filetime.md) que contêm os valores de hora. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre o PT_MV_SYSTIME, confira [lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


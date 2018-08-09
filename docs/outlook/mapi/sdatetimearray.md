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
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770333"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de valores de hora são usadas para descrever uma propriedade do tipo PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpft** . 
    
 **lpft**
  
> Ponteiro para uma matriz de estruturas [FILETIME](filetime.md) que contêm os valores de tempo. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_SYSTIME, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


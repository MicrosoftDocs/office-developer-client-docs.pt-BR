---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770441"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de valores de cadeia de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_STRING8.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lppszA** . 
    
 **lppszA**
  
> Ponteiro para uma matriz de cadeias de caracteres de 8 bits terminou de null.
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_STRING8, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


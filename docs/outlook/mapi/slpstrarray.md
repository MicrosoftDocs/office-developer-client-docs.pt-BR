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
ms.openlocfilehash: ccad74a9f2553bf29af124821c6d6a87dcde3303
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572869"
---
# <a name="slpstrarray"></a>SLPSTRArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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


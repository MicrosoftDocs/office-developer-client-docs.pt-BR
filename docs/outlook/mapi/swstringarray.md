---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770553"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de cadeias de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de cadeias de caracteres na matriz apontado pelo membro **lppszW** . 
    
 **lppszW**
  
> Ponteiro para uma matriz de cadeias de caracteres Unicode null-encerrada.
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_UNICODE, consulte [Tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


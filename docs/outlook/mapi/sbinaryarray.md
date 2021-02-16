---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438285"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores binários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontada pelo membro **lpbin.** 
    
 **lpbin**
  
> Ponteiro para uma matriz de [estruturas SBinary](sbinary.md) que contém os valores binários. 
    
## <a name="remarks"></a>Comentários

A **estrutura SBinaryArray** é usada para descrever propriedades do tipo PT_MV_BINARY. 
  
Para obter mais informações sobre PT_MV_BINARY, consulte [Lista de tipos de propriedade.](property-types.md)
  
## <a name="see-also"></a>Confira também



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


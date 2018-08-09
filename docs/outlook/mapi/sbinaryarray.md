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
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770294"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Aplica-se a**: Outlook 
  
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
  
> Contagem de valores na matriz apontado pelo membro **lpbin** . 
    
 **lpbin**
  
> Ponteiro para uma matriz de estruturas de [SBinary](sbinary.md) que contém os valores binários. 
    
## <a name="remarks"></a>Comentários

A estrutura **SBinaryArray** é usada para descrever as propriedades do tipo PT_MV_BINARY. 
  
Para obter mais informações sobre PT_MV_BINARY, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


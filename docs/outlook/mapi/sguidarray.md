---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19770397"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas [GUID](guid.md) que são usadas para descrever uma propriedade do tipo PT_MV_CLSID. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpguid** . 
    
 **lpguid**
  
> Ponteiro para uma matriz de estruturas **GUID** que contém os valores de identificador de classe. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_CLSID, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


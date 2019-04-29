---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430382"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores de tempo.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontada pelo membro **lpat** . 
    
 **lpat**
  
> Ponteiro para uma matriz de valores de tempo de aplicativo. 
    
## <a name="remarks"></a>Comentários

A estrutura **SAppTimeArray** é usada para definir propriedades do tipo PT_MV_APPTIME. Para obter mais informações sobre o PT_MV_APPTIME, confira [lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)


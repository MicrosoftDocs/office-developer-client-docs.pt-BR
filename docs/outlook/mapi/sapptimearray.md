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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770286"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de valores de tempo.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpat** . 
    
 **lpat**
  
> Ponteiro para uma matriz de valores de tempo do aplicativo. 
    
## <a name="remarks"></a>Comentários

A estrutura **SAppTimeArray** é usada para definir as propriedades do tipo PT_MV_APPTIME. Para obter mais informações sobre PT_MV_APPTIME, consulte a [Lista de tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[Estruturas MAPI](mapi-structures.md)


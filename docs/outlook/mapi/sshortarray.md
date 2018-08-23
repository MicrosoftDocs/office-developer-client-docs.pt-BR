---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573030"
---
# <a name="sshortarray"></a>SShortArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores de inteiro não assinado que são usadas para descrever uma propriedade do tipo PT_MV_SHORT.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpi** . 
    
 **lpi**
  
> Ponteiro para uma matriz de valores de inteiro não assinado.
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre PT_MV_SHORT e outros tipos de propriedade, consulte [Tipos de propriedade](property-types.md). 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


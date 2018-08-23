---
title: SCurrencyArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCurrencyArray
api_type:
- COM
ms.assetid: d28852ab-b542-40e1-b2ec-85d20a2eddfd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1b262ba9c83e9890719f716a373c566be172ae73
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572449"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores de moeda que são usadas para descrever uma propriedade do tipo PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontado pelo membro **lpcur** . 
    
 **lpcur**
  
> Ponteiro para uma matriz de estruturas de [moeda](currency.md) que contêm os valores de moeda. 
    
## <a name="remarks"></a>Comentários

Para obter informações sobre PT_MV_CURRENCY, consulte a [Lista de tipos de propriedade](property-types.md). 
  
## <a name="see-also"></a>Confira também



[CURRENCY](currency.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


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
ms.openlocfilehash: c440bb7d8f3d2d3002a4d1a80ca3a671b49f4d2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770343"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Aplica-se a**: Outlook 
  
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


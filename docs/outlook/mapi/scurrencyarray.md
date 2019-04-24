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
ms.openlocfilehash: e9468d0c7fc7e46475afe19f12f225e53196639e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360694"
---
# <a name="scurrencyarray"></a>SCurrencyArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de valores de moeda que são usados para descrever uma propriedade do tipo PT_MV_CURRENCY. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SCurrencyArray
{
  ULONG         cValues;
  CURRENCY FAR *lpcur;
} SCurrencyArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores na matriz apontada pelo membro **lpcur** . 
    
 **lpcur**
  
> Ponteiro para uma matriz de estruturas de [moeda](currency.md) que contêm os valores de moeda. 
    
## <a name="remarks"></a>Comentários

Para obter informações sobre o PT_MV_CURRENCY, consulte [list of Property Types](property-types.md). 
  
## <a name="see-also"></a>Confira também



[MOEDA](currency.md)
  
[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


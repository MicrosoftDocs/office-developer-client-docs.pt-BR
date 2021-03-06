---
title: CURRENCY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CURRENCY
api_type:
- COM
ms.assetid: cffc05a0-95e4-4b9f-bf8f-c4272a75afa8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dccb6b19af72d0f748a3a513b7f3d78904ebc789
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431117"
---
# <a name="currency"></a>CURRENCY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um inteiro de 64 bits assinado que representa um valor de moeda. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Lo**
  
> 32 bits de ordem baixa do valor da moeda. 
    
 **Olá**
  
> 32 bits de ordem alta do valor da moeda.
    
## <a name="remarks"></a>Comentários

A **estrutura CURRENCY** é uma representação inteira dimensionada de um número decimal com quatro dígitos à direita da vírgula decimal. Por exemplo, um valor armazenado de 327500 deve ser interpretado como representando um valor de moeda de 32,7500. 
  
A **estrutura CURRENCY** é usada para descrever uma propriedade do tipo PT_CURRENCY. Para obter informações sobre tipos de propriedade, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


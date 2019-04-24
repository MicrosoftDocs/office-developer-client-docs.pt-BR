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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315131"
---
# <a name="currency"></a>CURRENCY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um inteiro de 64 bits assinado que representa um valor de moeda. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct tagCY
{
  unsigned long Lo;
  long Hi;
} CURRENCY;

```

## <a name="members"></a>Members

 **Baixo**
  
> Bits de 32 de ordem inferior do valor de moeda. 
    
 **Oi**
  
> Alta ordem 32 bits do valor da moeda.
    
## <a name="remarks"></a>Comentários

A estrutura de **moeda** é uma representação inteira em escala de um número decimal com quatro dígitos à direita da vírgula decimal. Por exemplo, um valor armazenado de 327500 deve ser interpretado como representando um valor de moeda de 32,7500. 
  
A estrutura de **moeda** é usada para descrever uma propriedade do tipo PT_CURRENCY. Para obter informações sobre tipos de propriedade, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0789b566eb814fe984ae78670d22ad2937b0c3a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766368"
---
# <a name="currency"></a>CURRENCY

  
  
**Aplica-se a**: Outlook 
  
Contém um inteiro assinado de 64 bits representando um valor de moeda. 
  
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

## <a name="members"></a>Membros

 **Lo**
  
> Ordem baixa de 32 bits do valor de moeda. 
    
 **Oi**
  
> Ordem alta de 32 bits do valor de moeda.
    
## <a name="remarks"></a>Coment�rios

A estrutura de **moeda** é uma representação de inteiro em escala de um número decimal com quatro dígitos à direita da vírgula decimal. Por exemplo, um valor armazenado de 327500 deve ser interpretado como representando um valor de moeda da 32.7500. 
  
A estrutura de **moeda** é usada para descrever uma propriedade do tipo PT_CURRENCY. Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


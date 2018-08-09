---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770291"
---
# <a name="sbinary"></a>SBinary

  
  
**Aplica-se a**: Outlook 
  
Descreve uma propriedade do tipo PT_BINARY.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> Contagem de bytes no membro **lpb** . 
    
 **lpb**
  
> Ponteiro para o valor da propriedade PT_BINARY.
    
## <a name="remarks"></a>Comentários

Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


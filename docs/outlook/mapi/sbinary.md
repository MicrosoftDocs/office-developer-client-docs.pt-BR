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
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407841"
---
# <a name="sbinary"></a>SBinary

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> Contagem de bytes no **membro lpb.** 
    
 **lpb**
  
> Ponteiro para o valor PT_BINARY propriedade.
    
## <a name="remarks"></a>Comentários

Para obter informações sobre tipos de propriedade, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)


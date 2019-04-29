---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426650"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição **not** , que é usada para aplicar uma operação lógica **not** a uma restrição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> no Serve deve ser zero.
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) descrevendo a restrição a ser associada ao operador lógico **not** . 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre a estrutura **SNotRestriction** , consulte [about Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


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
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575060"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição **não** , que é usada para aplicar uma operação **não é** lógica para uma restrição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Members

 **ulReserved**
  
> [in] Reservado; deve ser zero.
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) descrevendo a restrição de estar associado ao operador **não é** lógico. 
    
## <a name="remarks"></a>Comentários

Para obter mais informações sobre a estrutura **SNotRestriction** , consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


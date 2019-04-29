---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438880"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição **e** que é usada para ingressar em um grupo de restrições usando uma operação **e** lógica. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Contagem de restrições de pesquisa na matriz apontada pelo membro **lpRes** . 
    
 **lpRes**
  
> Ponteiro para uma matriz de estruturas [SRestriction](srestriction.md) que serão combinadas com uma operação **e** lógica. 
    
## <a name="remarks"></a>Comentários

O resultado da **SAndRestriction** será true se todas as restrições filhas forem avaliadas como true. É FALSE se qualquer restrição de filho é avaliada como FALSE. 
  
Para obter uma descrição dos tipos de restrições, como criá-los e código de exemplo, consulte [about Restrictions](about-restrictions.md).
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


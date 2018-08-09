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
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770304"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Aplica-se a**: Outlook 
  
Descreve uma restrição **AND** , que é utilizada para ingressar em um grupo de restrições usando uma operação **AND** lógica. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Contagem de restrições de pesquisa na matriz apontado pelo membro **lpRes** . 
    
 **lpRes**
  
> Ponteiro para uma matriz de estruturas [SRestriction](srestriction.md) que será combinado com uma operação **AND** lógica. 
    
## <a name="remarks"></a>Comentários

O resultado do **SAndRestriction** é TRUE se todas as restrições de seu filho é avaliada como verdadeiro. Ele é FALSE se qualquer restrição de filhos for falso. 
  
Para obter uma descrição dos tipos de restrições, como criá-los e código de exemplo, consulte [Sobre restrições](about-restrictions.md).
  
## <a name="see-also"></a>Confira também



[SRestriction](srestriction.md)


[Estruturas MAPI](mapi-structures.md)


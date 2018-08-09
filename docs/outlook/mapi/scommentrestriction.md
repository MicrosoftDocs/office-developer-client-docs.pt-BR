---
title: SCommentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SCommentRestriction
api_type:
- COM
ms.assetid: 07631ae1-981e-4c8e-a30b-1213904fe079
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2185b059f2b831a14b90bad3a3c286ed72f8234d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770318"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Aplica-se a**: Outlook 
  
Descreve uma restrição de comentário, que é usada para anotar uma restrição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SCommentRestriction
{
  ULONG          cValues;
  LPSRestriction lpRes;
  LPSPropValue   lpProp;
} SCommentRestriction;

```

## <a name="members"></a>Members

 **cValues**
  
> Contagem de valores de propriedade na matriz apontado pelo membro **lpProp** . 
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) , cada um contendo a marca de propriedade e o valor de uma propriedade nomeada. 
    
## <a name="remarks"></a>Comentários

A estrutura **SCommentRestriction** associa um objeto junto com um conjunto de propriedades nomeadas. Restrições de comentário são Diferentemente de outras restrições, pois eles não são avaliados. Ou seja, eles são ignorados pelo método [IMAPITable:: Restrict](imapitable-restrict.md) . Não há nenhum efeito sobre as linhas retornadas pelo método [IMAPITable:: QueryRows](imapitable-queryrows.md) após ter sido feita uma chamada **IMAPITable:: Restrict** . 
  
A estrutura de **SCommentRestriction** pode ser usada para manter informações específicas do aplicativo com uma restrição quando ele for salvo no disco. Por exemplo, um cliente a salvando o nome de uma propriedade nomeada usado em uma restrição de propriedade poderá fazer isso em uma estrutura **SCommentRestriction** . Salvar um nome de propriedade não é possível em uma restrição de propriedade, porque a estrutura de [SPropertyRestriction](spropertyrestriction.md) associada contém apenas a marca de propriedade. 
  
Para obter mais informações sobre a estrutura de **SCommentRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Estruturas MAPI](mapi-structures.md)


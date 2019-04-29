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
ms.openlocfilehash: 3f66f513cc16bc479dd24c53804d751a396141f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430606"
---
# <a name="scommentrestriction"></a>SCommentRestriction

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma restrição de comentário, que é usada para anotar uma restrição. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Contagem de valores de propriedade na matriz apontada pelo membro **lpProp** . 
    
 **lpRes**
  
> Ponteiro para uma estrutura [SRestriction](srestriction.md) . 
    
 **lpProp**
  
> Ponteiro para uma matriz de estruturas [SPropValue](spropvalue.md) , cada uma contendo a marca de propriedade e o valor de uma propriedade nomeada. 
    
## <a name="remarks"></a>Comentários

A estrutura **SCommentRestriction** associa um objeto junto a um conjunto de propriedades nomeadas. As restrições de comentário são diferentes de outras restrições porque elas não são avaliadas. Ou seja, eles são ignorados pelo método imApitable [:: Restrict](imapitable-restrict.md) . Não há efeito nas linhas retornadas pelo método imApitable [:: QueryRows](imapitable-queryrows.md) após uma chamada IMAPITable **:: Restrict** foi feita. 
  
A estrutura **SCommentRestriction** pode ser usada para manter as informações específicas do aplicativo com uma restrição quando salva no disco. Por exemplo, um cliente que salva o nome de uma propriedade nomeada usada em uma restrição de propriedade pode fazê-lo em uma estrutura **SCommentRestriction** . Não é possível salvar um nome de propriedade em uma restrição de propriedade porque a estrutura [SPropertyRestriction](spropertyrestriction.md) associada contém apenas a marca de propriedade. 
  
Para obter mais informações sobre a estrutura e as restrições do **SCommentRestriction** em geral, consulte [about Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)
  
[SRestriction](srestriction.md)
  
[SPropertyRestriction](spropertyrestriction.md)


[Estruturas MAPI](mapi-structures.md)


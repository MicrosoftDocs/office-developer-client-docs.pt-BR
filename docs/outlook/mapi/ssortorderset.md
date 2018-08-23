---
title: SSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrderSet
api_type:
- COM
ms.assetid: e7f9be6a-92e7-44a8-93ee-b087713a31df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8d85ba55c5aa2f3780ad8e04cf1326cd7c35865
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575935"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma coleção de chaves de classificação para uma tabela que é usado para a classificação padrão ou categorizados.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md) <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a>Members

 **cSorts**
  
> Contagem de estruturas de [SSortOrder](ssortorder.md) que estão incluídos no membro **aSort** . 
    
 **cCategories**
  
> Contagem de colunas que são designados como colunas de categoria. Intervalo de valores possíveis de zero, o que indica uma classificação padrão ou não categorizadas, ao número indicado pelo membro **cSorts** . 
    
 **cExpanded**
  
> Contagem de categorias que iniciar em um estado expandido, onde todas as linhas que se aplicam à categoria são visíveis no modo de exibição de tabela. Intervalo de valores possíveis de 0 ao número indicado pelo **cCategories**.
    
 **aSort**
  
> Matriz de estruturas de **SSortOrder** , cada um definindo uma ordem de classificação. 
    
## <a name="remarks"></a>Comentários

Uma estrutura de **SSortOrderSet** é usada para definir várias ordens de classificação para a classificação padrão e categorizados. 
  
Cada estrutura **SSortOrderSet** contém pelo menos uma estrutura de **SSortOrder** definindo a direção da classificação e a coluna que será usada como a chave de classificação. Para que a classificação categorizada, esta coluna é usada como a categoria. Quando o valor do membro **cSorts** excede o valor do membro **cCategories** , há mais chaves de classificação que categorias e categorias são criadas a partir de colunas que aparecem primeira na matriz **SSortOrder** . 
  
Por exemplo, se **cSorts** for definido como 3 e **cCategories** é definida como 2, as colunas descritas pelo membro **ulPropTag** das duas primeiras entradas na matriz **SSortOrder** são usadas como as colunas de categoria. A primeira entrada serve como a categoria de nível superior de agrupamento; a segunda entrada como o agrupamento secundário. Todas as linhas que coincidem com as colunas de duas categorias são classificadas por meio da chave de classificação definida na terceira entrada. 
  
O membro **cExpanded** Especifica o número de categorias que estão em um primeiro momento expandido. Quando houver várias categorias, a implementação de tabela começa com a primeira coluna que será designado como uma categoria e continua em ordem sequencial com as colunas de categoria subsequentes, até que o número de **cCategories** foi excedido. Se houver mais colunas de categoria que existem colunas expandidas, as colunas de categoria são contraídas. Se **cExpanded** for igual a zero, somente a linha do cabeçalho de nível superior está disponível para o usuário de tabela para exibição. Se **cExpanded** for igual a menos que o número de categorias, em seguida, todas as linhas de cabeçalho e nenhuma das linhas folha estão disponíveis. Se **cExpanded** for igual ao número de categorias, a tabela é totalmente expandida. 
  
Para obter mais informações sobre a classificação padrão e categorizados, consulte [classificação e categorização](sorting-and-categorization.md).
  
## <a name="see-also"></a>Confira também



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Estruturas MAPI](mapi-structures.md)


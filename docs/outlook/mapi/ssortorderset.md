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
ms.openlocfilehash: db19c3908c419b98b8deb71e2a86d0aa6eebe240
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438096"
---
# <a name="ssortorderset"></a>SSortOrderSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma coleção de chaves de classificação para uma tabela que é usada para classificação padrão ou categorizada.
  
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
  
> Contagem de [estruturas SSortOrder](ssortorder.md) incluídas no **membro aSort.** 
    
 **cCategories**
  
> Contagem de colunas designadas como colunas de categoria. Os valores possíveis variam de zero, que indica uma classificação não categorizada ou padrão, até o número indicado pelo membro **cSorts.** 
    
 **cExpanded**
  
> Contagem de categorias que começam em um estado expandido, onde todas as linhas que se aplicam à categoria são visíveis no exibição de tabela. Os valores possíveis vão de 0 ao número indicado por **cCategories**.
    
 **aSort**
  
> Matriz de **estruturas SSortOrder,** cada uma definindo uma ordem de classificação. 
    
## <a name="remarks"></a>Comentários

Uma **estrutura SSortOrderSet** é usada para definir várias ordens de classificação para classificação padrão e categorizada. 
  
Cada **estrutura SSortOrderSet** contém pelo menos uma estrutura **SSortOrder** definindo a direção da classificação e a coluna que será usada como a chave de classificação. Para classificação categorizada, essa coluna é usada como categoria. Quando o valor do membro **cSorts** excede o valor do membro **cCategories,** há mais chaves de classificação do que categorias, e as categorias são criadas a partir das colunas que aparecem primeiro na matriz **SSortOrder.** 
  
Por exemplo, se **cSorts** for definido como 3 e **cCategories** for definido como 2, as colunas descritas pelo membro **ulPropTag** das duas primeiras entradas na matriz **SSortOrder** serão usadas como colunas de categoria. A primeira entrada serve como o grupo de categorias de nível superior; a segunda entrada como o grupo secundário. Todas as linhas que corresponderem às duas colunas de categoria são ordenadas usando a chave de classificação definida na terceira entrada. 
  
O **membro cExpanded** especifica o número de categorias que estão na primeira expansão. Quando há várias categorias, a implementação da tabela começa com a primeira coluna a ser designada como uma categoria e continua em ordem sequencial com as colunas de categoria subsequentes até que o número de **cCategories** seja excedido. Se houver mais colunas de categoria do que colunas expandidas, as colunas de categoria serão recolhidos. Se **cExpanded for** igual a zero, somente a linha de título de nível superior estará disponível para exibição do usuário da tabela. Se **cExpanded** for igual a um a menos que o número de categorias, todas as linhas de título e nenhuma das linhas folha estarão disponíveis. Se **cExpanded for** igual ao número de categorias, a tabela será totalmente expandida. 
  
Para obter mais informações sobre classificação padrão e categorizada, consulte [Classificação e Categorização.](sorting-and-categorization.md)
  
## <a name="see-also"></a>Confira também



[SSortOrder](ssortorder.md)
  
[IMAPITable::ExpandRow](imapitable-expandrow.md)
  
[IMAPITable::CollapseRow](imapitable-collapserow.md)


[Estruturas MAPI](mapi-structures.md)


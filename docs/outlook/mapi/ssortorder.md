---
title: SSortOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSortOrder
api_type:
- COM
ms.assetid: fe181b9a-5903-4cc0-bcd5-2061b440b5b1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f9d38c90fa5795d34f78c61ce0faa5f76d8f740d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439720"
---
# <a name="ssortorder"></a>SSortOrder
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define como classificar as linhas de uma tabela, qual coluna usar como a chave de classificação e a direção da classificação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a>Members

**ulPropTag**
  
> Marca de propriedade que identifica a chave de classificação ou, para uma classificação categorizada, a coluna de categoria.
    
**ulOrder**
  
> A ordem na qual os dados devem ser organizados. Os valores possíveis são:
    
  - TABLE_SORT_ASCEND: a tabela deve ser ordenada em ordem crescente.
      
  - TABLE_SORT_COMBINE: a operação de classificação deve criar uma categoria que combine a propriedade identificada como a coluna de chave de classificação no membro **ulPropTag** com a coluna de chave de classificação especificada na estrutura **SSortOrder** anterior. 
      
    TABLE_SORT_COMBINE pode ser usado somente quando a estrutura **SSortOrder** está sendo usada como uma entrada em uma estrutura [SSortOrderSet](ssortorderset.md) para especificar várias ordens de classificação para uma classificação categorizada. TABLE_SORT_COMBINE pode ser usado na primeira **estrutura SSortOrder** em uma **estrutura SSortOrderSet.** 
      
  - TABLE_SORT_DESCEND: a tabela deve ser ordenada em ordem decrescente.
      
  - TABLE_SORT_CATEG_MAX: a tabela deve ser ordenada no valor máximo do membro **ulPropTag** para as linhas de dados nas categorias especificadas pela ordem de classificação anterior na estrutura **SSortOrderSet.** 
      
  - TABLE_SORT_CATEG_MIN: a tabela deve ser ordenada no valor mínimo do membro **ulPropTag** para as linhas de dados nas categorias especificadas pela ordem de classificação anterior na estrutura **SSortOrderSet.** 
    
## <a name="remarks"></a>Comentários

Uma **estrutura SSortOrder** é usada para descrever como executar uma operação de classificação padrão ou uma operação de classificação categorizada. **Estruturas SSortOrder** geralmente são combinadas em uma estrutura **SSortOrderSet** para descrever várias chaves de classificação e trajetos. **As estruturas SSortOrderSet** são usadas nas seguintes funções e métodos de interface: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
O intervalo de colunas permitidas em uma tabela que pode ser usada como uma chave de classificação depende do provedor. As colunas que fazem parte do conjunto de colunas atual sempre podem ser usadas como chaves de classificação. No entanto, cada provedor determina se as chaves de classificação podem ser definidas usando colunas disponíveis que não estão no conjunto de colunas atual. Uma coluna disponível é uma coluna retornada de [IMAPITable::QueryColumns](imapitable-querycolumns.md) quando o sinalizador TBL_ALL_COLUMNS está definido. 
  
O **membro ulOrder** indica a ordem direcional e as informações de categorização, por exemplo, por conversa ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), ou seja, thread de conversa, que é uma série de mensagens e respostas. As linhas podem ser ordenadas em uma sequência crescente ou decrescente com todas as entradas NULL posicionadas por último. 
  
O TABLE_SORT_COMBINE valor indica que a coluna especificada em **ulPropTag** deve ser combinada com a coluna de categoria anterior para formar uma categoria composta. Ou seja, em vez de categorizar valores exclusivos de colunas individuais, TABLE_SORT_COMBINE permite categorização em valores exclusivos de uma combinação de colunas. Por exemplo, uma única categoria poderia ser definida para agrupar mensagens recebidas de um remetente específico em um determinado assunto. Definir o valor como TABLE_SORT_COMBINE reduz o número de linhas de categoria que são exibidas. 
  
A classificação em colunas de valores múltiplos não é universalmente suportada por todas as implementações de tabela. Se tiver suporte, aplique o MV_FLAG usando a macro MVI_PROP à marca de propriedade no membro **ulPropTag** para identificar a chave de classificação como uma coluna de vários valores. A classificação em uma coluna de valores múltiplos baseia-se no uso dos valores individuais. 
  
> [!IMPORTANT]
> Os valores de membro **ulOrder** TABLE_SORT_CATEG_MAX e TABLE_SORT_CATEG_MIN podem não ser definidos no arquivo de header baixável que você tem atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Para obter mais informações sobre classificação padrão e categorizada, consulte [Classificação e Categorização.](sorting-and-categorization.md) 
  
## <a name="see-also"></a>Confira também

- [SSortOrderSet](ssortorderset.md)
- [Estruturas MAPI](mapi-structures.md)


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
ms.openlocfilehash: 331dc05b30390bb803d186f157e0fe9edb779ab0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571665"
---
# <a name="ssortorder"></a>SSortOrder
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define como classificar as linhas de uma tabela, quais coluna a ser usado como a chave de classificação e a direção da classificação. 
  
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
  
> Marca de propriedade que identifica a classificação principal ou, para uma classificação categorizada, a coluna categoria.
    
**ulOrder**
  
> A ordem na qual os dados são a ser classificado. Valores possíveis são os seguintes:
    
  - TABLE_SORT_ASCEND: A tabela deve ser classificada em ordem crescente.
      
  - TABLE_SORT_COMBINE: A operação de classificação deve criar uma categoria que combina a propriedade identificada como a coluna de chaves de classificação no membro **ulPropTag** com a coluna de chaves de classificação especificada na estrutura **SSortOrder** anterior. 
      
    TABLE_SORT_COMBINE só pode ser usado quando a estrutura **SSortOrder** está sendo usada como uma entrada em uma estrutura de [SSortOrderSet](ssortorderset.md) para especificar diversas ordens de classificação para uma classificação categorizada. TABLE_SORT_COMBINE não pode ser usado na estrutura de **SSortOrder** primeira em uma estrutura **SSortOrderSet** . 
      
  - TABLE_SORT_DESCEND: A tabela deve ser classificada em ordem decrescente.
      
  - TABLE_SORT_CATEG_MAX: A tabela deve ser classificada no valor máximo do membro **ulPropTag** para as linhas de dados em categorias especificadas pela ordem de classificação anterior na estrutura de **SSortOrderSet** . 
      
  - TABLE_SORT_CATEG_MIN: A tabela deve ser classificada em que o valor mínimo do membro **ulPropTag** para as linhas de dados em categorias especificadas pela ordem de classificação anterior na estrutura de **SSortOrderSet** em. 
    
## <a name="remarks"></a>Comentários

Uma estrutura de **SSortOrder** é usada para descrever como executar uma operação de classificação padrão ou uma operação de classificação categorizados. Estruturas de **SSortOrder** geralmente são combinadas em uma estrutura de **SSortOrderSet** para descrever várias chaves de classificação e direções. Estruturas de **SSortOrderSet** são usadas as seguintes funções e os métodos de interface: 
  
- [ITableData::HrGetView](itabledata-hrgetview.md)
    
- [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)
    
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
O intervalo de colunas permitidas em uma tabela que pode ser usado como uma chave de classificação depende do provedor. Colunas que fazem parte do conjunto de coluna atual sempre podem ser usadas como chaves de classificação. No entanto, cada provedor determina se as chaves de classificação podem ser definidas usando colunas disponíveis não na coluna atual definidas. Uma coluna disponível é uma coluna que é retornada por [IMAPITable::QueryColumns](imapitable-querycolumns.md) quando o sinalizador TBL_ALL_COLUMNS está definido. 
  
O membro **ulOrder** indica ordem direcional e informações de categorização, por exemplo, por conversa ([Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), ou seja, thread conversação, que é uma série de mensagens e respostas. Linhas podem ser classificadas em ordem crescente ou decrescente sequência com todas as entradas NULL posicionadas última. 
  
O valor TABLE_SORT_COMBINE indica que a coluna especificada em **ulPropTag** deve ser combinada com a coluna Categoria anterior para formar uma categoria composto. Ou seja, em vez de categorização nos valores exclusivos de colunas individuais, TABLE_SORT_COMBINE permite a categorização de valores exclusivos de uma combinação de colunas. Por exemplo, uma única categoria pode ser definida para agrupar mensagens recebidas de um remetente específico em um determinado assunto. Definindo o valor para TABLE_SORT_COMBINE reduz o número de linhas de categoria que são exibidos. 
  
Não há suporte universal ao classificando colunas de valores múltiplos por todas as implementações de tabela. Se houver suporte, aplique o MV_FLAG usando a macro MVI_PROP como a marca de propriedade no membro **ulPropTag** para identificar a chave de classificação como uma coluna de valores múltiplos. Classificando em uma coluna de valores múltiplos se baseia em usando os valores individuais. 
  
> [!IMPORTANT]
> Os valores de membro **ulOrder** TABLE_SORT_CATEG_MAX e TABLE_SORT_CATEG_MIN não podem ser definidos no arquivo de cabeçalho de página de download você possui atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`
  
Para obter mais informações sobre a classificação padrão e categorizados, consulte [classificação e categorização](sorting-and-categorization.md). 
  
## <a name="see-also"></a>Confira também

- [SSortOrderSet](ssortorderset.md)
- [Estruturas MAPI](mapi-structures.md)


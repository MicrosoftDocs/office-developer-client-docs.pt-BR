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
# <a name="ssortorder"></a><span data-ttu-id="a166d-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="a166d-103">SSortOrder</span></span>
 
<span data-ttu-id="a166d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a166d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a166d-105">Define como classificar as linhas de uma tabela, qual coluna usar como a chave de classificação e a direção da classificação.</span><span class="sxs-lookup"><span data-stu-id="a166d-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a166d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a166d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a166d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a166d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="a166d-108">Members</span><span class="sxs-lookup"><span data-stu-id="a166d-108">Members</span></span>

<span data-ttu-id="a166d-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="a166d-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="a166d-110">Marca de propriedade que identifica a chave de classificação ou, para uma classificação categorizada, a coluna de categoria.</span><span class="sxs-lookup"><span data-stu-id="a166d-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="a166d-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="a166d-111">**ulOrder**</span></span>
  
> <span data-ttu-id="a166d-112">A ordem na qual os dados devem ser organizados.</span><span class="sxs-lookup"><span data-stu-id="a166d-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="a166d-113">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a166d-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="a166d-114">TABLE_SORT_ASCEND: a tabela deve ser ordenada em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="a166d-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="a166d-115">TABLE_SORT_COMBINE: a operação de classificação deve criar uma categoria que combine a propriedade identificada como a coluna de chave de classificação no membro **ulPropTag** com a coluna de chave de classificação especificada na estrutura **SSortOrder** anterior.</span><span class="sxs-lookup"><span data-stu-id="a166d-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="a166d-116">TABLE_SORT_COMBINE pode ser usado somente quando a estrutura **SSortOrder** está sendo usada como uma entrada em uma estrutura [SSortOrderSet](ssortorderset.md) para especificar várias ordens de classificação para uma classificação categorizada.</span><span class="sxs-lookup"><span data-stu-id="a166d-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="a166d-117">TABLE_SORT_COMBINE pode ser usado na primeira **estrutura SSortOrder** em uma **estrutura SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="a166d-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="a166d-118">TABLE_SORT_DESCEND: a tabela deve ser ordenada em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="a166d-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="a166d-119">TABLE_SORT_CATEG_MAX: a tabela deve ser ordenada no valor máximo do membro **ulPropTag** para as linhas de dados nas categorias especificadas pela ordem de classificação anterior na estrutura **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="a166d-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="a166d-120">TABLE_SORT_CATEG_MIN: a tabela deve ser ordenada no valor mínimo do membro **ulPropTag** para as linhas de dados nas categorias especificadas pela ordem de classificação anterior na estrutura **SSortOrderSet.**</span><span class="sxs-lookup"><span data-stu-id="a166d-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a166d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a166d-121">Remarks</span></span>

<span data-ttu-id="a166d-122">Uma **estrutura SSortOrder** é usada para descrever como executar uma operação de classificação padrão ou uma operação de classificação categorizada.</span><span class="sxs-lookup"><span data-stu-id="a166d-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="a166d-123">**Estruturas SSortOrder** geralmente são combinadas em uma estrutura **SSortOrderSet** para descrever várias chaves de classificação e trajetos.</span><span class="sxs-lookup"><span data-stu-id="a166d-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="a166d-124">**As estruturas SSortOrderSet** são usadas nas seguintes funções e métodos de interface:</span><span class="sxs-lookup"><span data-stu-id="a166d-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="a166d-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="a166d-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="a166d-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="a166d-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="a166d-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a166d-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="a166d-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a166d-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="a166d-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a166d-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="a166d-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="a166d-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="a166d-131">O intervalo de colunas permitidas em uma tabela que pode ser usada como uma chave de classificação depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="a166d-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="a166d-132">As colunas que fazem parte do conjunto de colunas atual sempre podem ser usadas como chaves de classificação.</span><span class="sxs-lookup"><span data-stu-id="a166d-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="a166d-133">No entanto, cada provedor determina se as chaves de classificação podem ser definidas usando colunas disponíveis que não estão no conjunto de colunas atual.</span><span class="sxs-lookup"><span data-stu-id="a166d-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="a166d-134">Uma coluna disponível é uma coluna retornada de [IMAPITable::QueryColumns](imapitable-querycolumns.md) quando o sinalizador TBL_ALL_COLUMNS está definido.</span><span class="sxs-lookup"><span data-stu-id="a166d-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="a166d-135">O **membro ulOrder** indica a ordem direcional e as informações de categorização, por exemplo, por conversa ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), ou seja, thread de conversa, que é uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="a166d-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="a166d-136">As linhas podem ser ordenadas em uma sequência crescente ou decrescente com todas as entradas NULL posicionadas por último.</span><span class="sxs-lookup"><span data-stu-id="a166d-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="a166d-137">O TABLE_SORT_COMBINE valor indica que a coluna especificada em **ulPropTag** deve ser combinada com a coluna de categoria anterior para formar uma categoria composta.</span><span class="sxs-lookup"><span data-stu-id="a166d-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="a166d-138">Ou seja, em vez de categorizar valores exclusivos de colunas individuais, TABLE_SORT_COMBINE permite categorização em valores exclusivos de uma combinação de colunas.</span><span class="sxs-lookup"><span data-stu-id="a166d-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="a166d-139">Por exemplo, uma única categoria poderia ser definida para agrupar mensagens recebidas de um remetente específico em um determinado assunto.</span><span class="sxs-lookup"><span data-stu-id="a166d-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="a166d-140">Definir o valor como TABLE_SORT_COMBINE reduz o número de linhas de categoria que são exibidas.</span><span class="sxs-lookup"><span data-stu-id="a166d-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="a166d-141">A classificação em colunas de valores múltiplos não é universalmente suportada por todas as implementações de tabela.</span><span class="sxs-lookup"><span data-stu-id="a166d-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="a166d-142">Se tiver suporte, aplique o MV_FLAG usando a macro MVI_PROP à marca de propriedade no membro **ulPropTag** para identificar a chave de classificação como uma coluna de vários valores.</span><span class="sxs-lookup"><span data-stu-id="a166d-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="a166d-143">A classificação em uma coluna de valores múltiplos baseia-se no uso dos valores individuais.</span><span class="sxs-lookup"><span data-stu-id="a166d-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="a166d-144">Os valores de membro **ulOrder** TABLE_SORT_CATEG_MAX e TABLE_SORT_CATEG_MIN podem não ser definidos no arquivo de header baixável que você tem atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="a166d-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="a166d-145">Para obter mais informações sobre classificação padrão e categorizada, consulte [Classificação e Categorização.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="a166d-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a166d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a166d-146">See also</span></span>

- [<span data-ttu-id="a166d-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a166d-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="a166d-148">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="a166d-148">MAPI Structures</span></span>](mapi-structures.md)


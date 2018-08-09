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
ms.openlocfilehash: 7cb511c7a021c4e65214acc7efa785be0e02ffc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770491"
---
# <a name="ssortorder"></a><span data-ttu-id="de2ad-103">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="de2ad-103">SSortOrder</span></span>
 
<span data-ttu-id="de2ad-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de2ad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de2ad-105">Define como classificar as linhas de uma tabela, quais coluna a ser usado como a chave de classificação e a direção da classificação.</span><span class="sxs-lookup"><span data-stu-id="de2ad-105">Defines how to sort the rows of a table, what column to use as the sort key, and the direction of the sort.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de2ad-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="de2ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="de2ad-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de2ad-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSortOrder
{
  ULONG ulPropTag;
  ULONG ulOrder;
} SSortOrder, FAR *LPSSortOrder;

```

## <a name="members"></a><span data-ttu-id="de2ad-108">Members</span><span class="sxs-lookup"><span data-stu-id="de2ad-108">Members</span></span>

<span data-ttu-id="de2ad-109">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="de2ad-109">**ulPropTag**</span></span>
  
> <span data-ttu-id="de2ad-110">Marca de propriedade que identifica a classificação principal ou, para uma classificação categorizada, a coluna categoria.</span><span class="sxs-lookup"><span data-stu-id="de2ad-110">Property tag identifying the sort key or, for a categorized sort, the category column.</span></span>
    
<span data-ttu-id="de2ad-111">**ulOrder**</span><span class="sxs-lookup"><span data-stu-id="de2ad-111">**ulOrder**</span></span>
  
> <span data-ttu-id="de2ad-112">A ordem na qual os dados são a ser classificado.</span><span class="sxs-lookup"><span data-stu-id="de2ad-112">The order in which the data is to be sorted.</span></span> <span data-ttu-id="de2ad-113">Valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="de2ad-113">Possible values are as follow:</span></span>
    
  - <span data-ttu-id="de2ad-114">TABLE_SORT_ASCEND: A tabela deve ser classificada em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="de2ad-114">TABLE_SORT_ASCEND: The table should be sorted in ascending order.</span></span>
      
  - <span data-ttu-id="de2ad-115">TABLE_SORT_COMBINE: A operação de classificação deve criar uma categoria que combina a propriedade identificada como a coluna de chaves de classificação no membro **ulPropTag** com a coluna de chaves de classificação especificada na estrutura **SSortOrder** anterior.</span><span class="sxs-lookup"><span data-stu-id="de2ad-115">TABLE_SORT_COMBINE: The sort operation should create a category that combines the property identified as the sort key column in the **ulPropTag** member with the sort key column specified in the previous **SSortOrder** structure.</span></span> 
      
    <span data-ttu-id="de2ad-116">TABLE_SORT_COMBINE só pode ser usado quando a estrutura **SSortOrder** está sendo usada como uma entrada em uma estrutura de [SSortOrderSet](ssortorderset.md) para especificar diversas ordens de classificação para uma classificação categorizada.</span><span class="sxs-lookup"><span data-stu-id="de2ad-116">TABLE_SORT_COMBINE can only be used when the **SSortOrder** structure is being used as an entry in an [SSortOrderSet](ssortorderset.md) structure to specify multiple sort orders for a categorized sort.</span></span> <span data-ttu-id="de2ad-117">TABLE_SORT_COMBINE não pode ser usado na estrutura de **SSortOrder** primeira em uma estrutura **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="de2ad-117">TABLE_SORT_COMBINE cannot be used in the first **SSortOrder** structure in an **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="de2ad-118">TABLE_SORT_DESCEND: A tabela deve ser classificada em ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="de2ad-118">TABLE_SORT_DESCEND: The table should be sorted in descending order.</span></span>
      
  - <span data-ttu-id="de2ad-119">TABLE_SORT_CATEG_MAX: A tabela deve ser classificada no valor máximo do membro **ulPropTag** para as linhas de dados em categorias especificadas pela ordem de classificação anterior na estrutura de **SSortOrderSet** .</span><span class="sxs-lookup"><span data-stu-id="de2ad-119">TABLE_SORT_CATEG_MAX: The table should be sorted on the maximum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the **SSortOrderSet** structure.</span></span> 
      
  - <span data-ttu-id="de2ad-120">TABLE_SORT_CATEG_MIN: A tabela deve ser classificada em que o valor mínimo do membro **ulPropTag** para as linhas de dados em categorias especificadas pela ordem de classificação anterior na estrutura de **SSortOrderSet** em.</span><span class="sxs-lookup"><span data-stu-id="de2ad-120">TABLE_SORT_CATEG_MIN: The table should be sorted on the minimum value of the **ulPropTag** member for the data rows in the categories specified by the previous sort order in the in **SSortOrderSet** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de2ad-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="de2ad-121">Remarks</span></span>

<span data-ttu-id="de2ad-122">Uma estrutura de **SSortOrder** é usada para descrever como executar uma operação de classificação padrão ou uma operação de classificação categorizados.</span><span class="sxs-lookup"><span data-stu-id="de2ad-122">An **SSortOrder** structure is used to describe how to perform either a standard sort operation or a categorized sort operation.</span></span> <span data-ttu-id="de2ad-123">Estruturas de **SSortOrder** geralmente são combinadas em uma estrutura de **SSortOrderSet** para descrever várias chaves de classificação e direções.</span><span class="sxs-lookup"><span data-stu-id="de2ad-123">**SSortOrder** structures are typically combined into an **SSortOrderSet** structure to describe multiple sort keys and directions.</span></span> <span data-ttu-id="de2ad-124">Estruturas de **SSortOrderSet** são usadas as seguintes funções e os métodos de interface:</span><span class="sxs-lookup"><span data-stu-id="de2ad-124">**SSortOrderSet** structures are used in the following functions and interface methods:</span></span> 
  
- [<span data-ttu-id="de2ad-125">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="de2ad-125">ITableData::HrGetView</span></span>](itabledata-hrgetview.md)
    
- [<span data-ttu-id="de2ad-126">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="de2ad-126">IMAPIFolder::SaveContentsSort</span></span>](imapifolder-savecontentssort.md)
    
- [<span data-ttu-id="de2ad-127">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="de2ad-127">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
    
- [<span data-ttu-id="de2ad-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="de2ad-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
- [<span data-ttu-id="de2ad-129">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="de2ad-129">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
- [<span data-ttu-id="de2ad-130">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="de2ad-130">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="de2ad-131">O intervalo de colunas permitidas em uma tabela que pode ser usado como uma chave de classificação depende do provedor.</span><span class="sxs-lookup"><span data-stu-id="de2ad-131">The range of allowed columns in a table that can be used as a sort key depends on the provider.</span></span> <span data-ttu-id="de2ad-132">Colunas que fazem parte do conjunto de coluna atual sempre podem ser usadas como chaves de classificação.</span><span class="sxs-lookup"><span data-stu-id="de2ad-132">Columns that are part of the current column set can always be used as sort keys.</span></span> <span data-ttu-id="de2ad-133">No entanto, cada provedor determina se as chaves de classificação podem ser definidas usando colunas disponíveis não na coluna atual definidas.</span><span class="sxs-lookup"><span data-stu-id="de2ad-133">However, each provider determines whether sort keys can be defined by using available columns that are not in the current column set.</span></span> <span data-ttu-id="de2ad-134">Uma coluna disponível é uma coluna que é retornada por [IMAPITable::QueryColumns](imapitable-querycolumns.md) quando o sinalizador TBL_ALL_COLUMNS está definido.</span><span class="sxs-lookup"><span data-stu-id="de2ad-134">An available column is a column that is returned from [IMAPITable::QueryColumns](imapitable-querycolumns.md) when the TBL_ALL_COLUMNS flag is set.</span></span> 
  
<span data-ttu-id="de2ad-135">O membro **ulOrder** indica ordem direcional e informações de categorização, por exemplo, por conversa ([Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md)), ou seja, thread conversação, que é uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="de2ad-135">The **ulOrder** member indicates both directional order and categorization information, for example, by conversation ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)), that is, conversational thread, which is a series of messages and replies.</span></span> <span data-ttu-id="de2ad-136">Linhas podem ser classificadas em ordem crescente ou decrescente sequência com todas as entradas NULL posicionadas última.</span><span class="sxs-lookup"><span data-stu-id="de2ad-136">Rows can be sorted in either an ascending or descending sequence with all NULL entries positioned last.</span></span> 
  
<span data-ttu-id="de2ad-137">O valor TABLE_SORT_COMBINE indica que a coluna especificada em **ulPropTag** deve ser combinada com a coluna Categoria anterior para formar uma categoria composto.</span><span class="sxs-lookup"><span data-stu-id="de2ad-137">The TABLE_SORT_COMBINE value indicates that the column specified in **ulPropTag** should be combined with the previous category column to form a composite category.</span></span> <span data-ttu-id="de2ad-138">Ou seja, em vez de categorização nos valores exclusivos de colunas individuais, TABLE_SORT_COMBINE permite a categorização de valores exclusivos de uma combinação de colunas.</span><span class="sxs-lookup"><span data-stu-id="de2ad-138">That is, instead of categorizing on unique values of individual columns, TABLE_SORT_COMBINE allows for categorization on unique values of a combination of columns.</span></span> <span data-ttu-id="de2ad-139">Por exemplo, uma única categoria pode ser definida para agrupar mensagens recebidas de um remetente específico em um determinado assunto.</span><span class="sxs-lookup"><span data-stu-id="de2ad-139">For example, a single category could be defined to group messages received from a particular sender on a particular subject.</span></span> <span data-ttu-id="de2ad-140">Definindo o valor para TABLE_SORT_COMBINE reduz o número de linhas de categoria que são exibidos.</span><span class="sxs-lookup"><span data-stu-id="de2ad-140">Setting the value to TABLE_SORT_COMBINE reduces the number of category rows that are displayed.</span></span> 
  
<span data-ttu-id="de2ad-141">Não há suporte universal ao classificando colunas de valores múltiplos por todas as implementações de tabela.</span><span class="sxs-lookup"><span data-stu-id="de2ad-141">Sorting on multi-valued columns is not universally supported by all table implementations.</span></span> <span data-ttu-id="de2ad-142">Se houver suporte, aplique o MV_FLAG usando a macro MVI_PROP como a marca de propriedade no membro **ulPropTag** para identificar a chave de classificação como uma coluna de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="de2ad-142">If supported, apply the MV_FLAG using the MVI_PROP macro to the property tag in the **ulPropTag** member to identify the sort key as a multi-valued column.</span></span> <span data-ttu-id="de2ad-143">Classificando em uma coluna de valores múltiplos se baseia em usando os valores individuais.</span><span class="sxs-lookup"><span data-stu-id="de2ad-143">Sorting on a multi-valued column is based on using the individual values.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="de2ad-144">Os valores de membro **ulOrder** TABLE_SORT_CATEG_MAX e TABLE_SORT_CATEG_MIN não podem ser definidos no arquivo de cabeçalho de página de download você possui atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span><span class="sxs-lookup"><span data-stu-id="de2ad-144">The **ulOrder** member values TABLE_SORT_CATEG_MAX and TABLE_SORT_CATEG_MIN might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following values: >  `#define TABLE_SORT_CATEG_MAX ((ULONG) 0x00000004)`>  `#define TABLE_SORT_CATEG_MIN ((ULONG) 0x00000008)`</span></span>
  
<span data-ttu-id="de2ad-145">Para obter mais informações sobre a classificação padrão e categorizados, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="de2ad-145">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de2ad-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="de2ad-146">See also</span></span>

- [<span data-ttu-id="de2ad-147">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="de2ad-147">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="de2ad-148">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="de2ad-148">MAPI Structures</span></span>](mapi-structures.md)


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
ms.openlocfilehash: 1604c4a1a0d1bf4008595b0d150b4f7eb3d1c2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770494"
---
# <a name="ssortorderset"></a><span data-ttu-id="9ac4e-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9ac4e-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="9ac4e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ac4e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ac4e-105">Define uma coleção de chaves de classificação para uma tabela que é usado para a classificação padrão ou categorizados.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ac4e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9ac4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ac4e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ac4e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9ac4e-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="9ac4e-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9ac4e-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="9ac4e-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="9ac4e-110">Members</span><span class="sxs-lookup"><span data-stu-id="9ac4e-110">Members</span></span>

 <span data-ttu-id="9ac4e-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-111">**cSorts**</span></span>
  
> <span data-ttu-id="9ac4e-112">Contagem de estruturas de [SSortOrder](ssortorder.md) que estão incluídos no membro **aSort** .</span><span class="sxs-lookup"><span data-stu-id="9ac4e-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="9ac4e-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-113">**cCategories**</span></span>
  
> <span data-ttu-id="9ac4e-114">Contagem de colunas que são designados como colunas de categoria.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="9ac4e-115">Intervalo de valores possíveis de zero, o que indica uma classificação padrão ou não categorizadas, ao número indicado pelo membro **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="9ac4e-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="9ac4e-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-116">**cExpanded**</span></span>
  
> <span data-ttu-id="9ac4e-117">Contagem de categorias que iniciar em um estado expandido, onde todas as linhas que se aplicam à categoria são visíveis no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="9ac4e-118">Intervalo de valores possíveis de 0 ao número indicado pelo **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="9ac4e-119">**aSort**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-119">**aSort**</span></span>
  
> <span data-ttu-id="9ac4e-120">Matriz de estruturas de **SSortOrder** , cada um definindo uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9ac4e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ac4e-121">Remarks</span></span>

<span data-ttu-id="9ac4e-122">Uma estrutura de **SSortOrderSet** é usada para definir várias ordens de classificação para a classificação padrão e categorizados.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="9ac4e-123">Cada estrutura **SSortOrderSet** contém pelo menos uma estrutura de **SSortOrder** definindo a direção da classificação e a coluna que será usada como a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="9ac4e-124">Para que a classificação categorizada, esta coluna é usada como a categoria.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="9ac4e-125">Quando o valor do membro **cSorts** excede o valor do membro **cCategories** , há mais chaves de classificação que categorias e categorias são criadas a partir de colunas que aparecem primeira na matriz **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="9ac4e-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="9ac4e-126">Por exemplo, se **cSorts** for definido como 3 e **cCategories** é definida como 2, as colunas descritas pelo membro **ulPropTag** das duas primeiras entradas na matriz **SSortOrder** são usadas como as colunas de categoria.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="9ac4e-127">A primeira entrada serve como a categoria de nível superior de agrupamento; a segunda entrada como o agrupamento secundário.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="9ac4e-128">Todas as linhas que coincidem com as colunas de duas categorias são classificadas por meio da chave de classificação definida na terceira entrada.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="9ac4e-129">O membro **cExpanded** Especifica o número de categorias que estão em um primeiro momento expandido.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="9ac4e-130">Quando houver várias categorias, a implementação de tabela começa com a primeira coluna que será designado como uma categoria e continua em ordem sequencial com as colunas de categoria subsequentes, até que o número de **cCategories** foi excedido.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="9ac4e-131">Se houver mais colunas de categoria que existem colunas expandidas, as colunas de categoria são contraídas.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="9ac4e-132">Se **cExpanded** for igual a zero, somente a linha do cabeçalho de nível superior está disponível para o usuário de tabela para exibição.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="9ac4e-133">Se **cExpanded** for igual a menos que o número de categorias, em seguida, todas as linhas de cabeçalho e nenhuma das linhas folha estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="9ac4e-134">Se **cExpanded** for igual ao número de categorias, a tabela é totalmente expandida.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="9ac4e-135">Para obter mais informações sobre a classificação padrão e categorizados, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="9ac4e-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ac4e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ac4e-136">See also</span></span>



[<span data-ttu-id="9ac4e-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="9ac4e-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="9ac4e-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="9ac4e-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="9ac4e-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="9ac4e-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="9ac4e-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9ac4e-140">MAPI Structures</span></span>](mapi-structures.md)


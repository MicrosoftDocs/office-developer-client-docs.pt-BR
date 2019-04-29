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
# <a name="ssortorderset"></a><span data-ttu-id="ee111-103">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ee111-103">SSortOrderSet</span></span>

  
  
<span data-ttu-id="ee111-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee111-105">Define uma coleção de chaves de classificação para uma tabela que é usada para classificação padrão ou categorizada.</span><span class="sxs-lookup"><span data-stu-id="ee111-105">Defines a collection of sort keys for a table that is used for standard or categorized sorting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee111-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ee111-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee111-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ee111-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ee111-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="ee111-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ee111-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span><span class="sxs-lookup"><span data-stu-id="ee111-109">[CbNewSSortOrderSet](cbnewssortorderset.md), [CbSSortOrderSet](cbssortorderset.md), [SizedSSortOrderSet](sizedssortorderset.md)</span></span> <br/> |
   
```cpp
typedef struct _SSortOrderSet
{
  ULONG cSorts;
  ULONG cCategories;
  ULONG cExpanded;
  SSortOrder aSort[MAPI_DIM];
} SSortOrderSet, FAR *LPSSortOrderSet;

```

## <a name="members"></a><span data-ttu-id="ee111-110">Members</span><span class="sxs-lookup"><span data-stu-id="ee111-110">Members</span></span>

 <span data-ttu-id="ee111-111">**cSorts**</span><span class="sxs-lookup"><span data-stu-id="ee111-111">**cSorts**</span></span>
  
> <span data-ttu-id="ee111-112">Contagem de estruturas [SSortOrder](ssortorder.md) incluídas no membro **classificação** .</span><span class="sxs-lookup"><span data-stu-id="ee111-112">Count of [SSortOrder](ssortorder.md) structures that are included in the **aSort** member.</span></span> 
    
 <span data-ttu-id="ee111-113">**cCategories**</span><span class="sxs-lookup"><span data-stu-id="ee111-113">**cCategories**</span></span>
  
> <span data-ttu-id="ee111-114">Contagem de colunas designadas como colunas de categoria.</span><span class="sxs-lookup"><span data-stu-id="ee111-114">Count of columns that are designated as category columns.</span></span> <span data-ttu-id="ee111-115">Os valores possíveis variam de zero, que indica uma classificação não categorizada ou padrão, para o número indicado pelo membro **cSorts** .</span><span class="sxs-lookup"><span data-stu-id="ee111-115">Possible values range from zero, which indicates a non-categorized or standard sort, to the number indicated by the **cSorts** member.</span></span> 
    
 <span data-ttu-id="ee111-116">**cExpanded**</span><span class="sxs-lookup"><span data-stu-id="ee111-116">**cExpanded**</span></span>
  
> <span data-ttu-id="ee111-117">Contagem de categorias que começam em um estado expandido, onde todas as linhas que se aplicam à categoria são visíveis no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="ee111-117">Count of categories that start in an expanded state, where all of the rows that apply to the category are visible in the table view.</span></span> <span data-ttu-id="ee111-118">Os valores possíveis variam de 0 até o número indicado por **cCategories**.</span><span class="sxs-lookup"><span data-stu-id="ee111-118">Possible values range from 0 to the number indicated by **cCategories**.</span></span>
    
 <span data-ttu-id="ee111-119">**Classificação**</span><span class="sxs-lookup"><span data-stu-id="ee111-119">**aSort**</span></span>
  
> <span data-ttu-id="ee111-120">Matriz de estruturas **SSortOrder** , cada uma definindo uma ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="ee111-120">Array of **SSortOrder** structures, each defining a sort order.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ee111-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee111-121">Remarks</span></span>

<span data-ttu-id="ee111-122">Uma estrutura **SSortOrderSet** é usada para definir várias ordens de classificação para classificação padrão e categorizada.</span><span class="sxs-lookup"><span data-stu-id="ee111-122">A **SSortOrderSet** structure is used for defining multiple sort orders for standard and categorized sorting.</span></span> 
  
<span data-ttu-id="ee111-123">Cada estrutura **SSortOrderSet** contém pelo menos uma estrutura **SSortOrder** que define a direção da classificação e a coluna que será usada como a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="ee111-123">Each **SSortOrderSet** structure contains at least one **SSortOrder** structure defining the direction of the sort and the column that will be used as the sort key.</span></span> <span data-ttu-id="ee111-124">Para classificação categorizada, esta coluna é usada como a categoria.</span><span class="sxs-lookup"><span data-stu-id="ee111-124">For categorized sorting, this column is used as the category.</span></span> <span data-ttu-id="ee111-125">Quando o valor do membro **cSorts** exceder o valor do membro **cCategories** , há mais chaves de classificação do que as categorias e as categorias são criadas a partir das colunas que aparecem primeiro na matriz **SSortOrder** .</span><span class="sxs-lookup"><span data-stu-id="ee111-125">When the value of the **cSorts** member exceeds the value of the **cCategories** member, there are more sort keys than categories, and categories are created from the columns that appear first in the **SSortOrder** array.</span></span> 
  
<span data-ttu-id="ee111-126">Por exemplo, se **cSorts** estiver definido como 3 e **cCategories** estiver definido como 2, as colunas descritas pelo membro **ulPropTag** das duas primeiras entradas na matriz **SSortOrder** serão usadas como colunas de categoria.</span><span class="sxs-lookup"><span data-stu-id="ee111-126">For example, if **cSorts** is set to 3 and **cCategories** is set to 2, the columns described by the **ulPropTag** member of the first two entries in the **SSortOrder** array are used as the category columns.</span></span> <span data-ttu-id="ee111-127">A primeira entrada serve como agrupamento de categorias de nível superior; a segunda entrada como o agrupamento secundário.</span><span class="sxs-lookup"><span data-stu-id="ee111-127">The first entry serves as the top-level category grouping; the second entry as the secondary grouping.</span></span> <span data-ttu-id="ee111-128">Todas as linhas que correspondem às duas colunas de categoria são classificadas usando a chave de classificação definida na terceira entrada.</span><span class="sxs-lookup"><span data-stu-id="ee111-128">All of the rows that match the two category columns are sorted by using the sort key defined in the third entry.</span></span> 
  
<span data-ttu-id="ee111-129">O membro **cExpanded** especifica o número de categorias que estão no primeiro expandidas.</span><span class="sxs-lookup"><span data-stu-id="ee111-129">The **cExpanded** member specifies the number of categories that are at first expanded.</span></span> <span data-ttu-id="ee111-130">Quando houver várias categorias, a implementação da tabela começará com a primeira coluna a ser designada como uma categoria e continuará em ordem sequencial com as colunas de categoria subsequentes até que o número de **cCategories** tenha sido excedido.</span><span class="sxs-lookup"><span data-stu-id="ee111-130">When there are multiple categories, the table implementation starts with the first column to be designated as a category and continues in sequential order with the subsequent category columns until the number of **cCategories** has been exceeded.</span></span> <span data-ttu-id="ee111-131">Se houver mais colunas de categoria do que as colunas expandidas, as colunas de categoria serão recolhidas.</span><span class="sxs-lookup"><span data-stu-id="ee111-131">If there are more category columns than there are expanded columns, the category columns are collapsed.</span></span> <span data-ttu-id="ee111-132">Se **cExpanded** for igual a zero, somente a linha de título de nível superior estará disponível para o usuário da tabela para exibição.</span><span class="sxs-lookup"><span data-stu-id="ee111-132">If **cExpanded** is equal to zero, only the top level heading row is available to the table user for display.</span></span> <span data-ttu-id="ee111-133">Se **cExpanded** for igual a um menor que o número de categorias, todas as linhas de título e nenhuma das linhas de folha estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ee111-133">If **cExpanded** is equal to one less than the number of categories, then all of the heading rows and none of the leaf rows are available.</span></span> <span data-ttu-id="ee111-134">Se **cExpanded** for igual ao número de categorias, a tabela estará totalmente expandida.</span><span class="sxs-lookup"><span data-stu-id="ee111-134">If **cExpanded** is equal to the number of categories, then the table is fully expanded.</span></span> 
  
<span data-ttu-id="ee111-135">Para obter mais informações sobre a classificação padrão e categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="ee111-135">For more information about standard and categorized sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee111-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee111-136">See also</span></span>



[<span data-ttu-id="ee111-137">SSortOrder</span><span class="sxs-lookup"><span data-stu-id="ee111-137">SSortOrder</span></span>](ssortorder.md)
  
[<span data-ttu-id="ee111-138">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ee111-138">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="ee111-139">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ee111-139">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)


[<span data-ttu-id="ee111-140">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ee111-140">MAPI Structures</span></span>](mapi-structures.md)


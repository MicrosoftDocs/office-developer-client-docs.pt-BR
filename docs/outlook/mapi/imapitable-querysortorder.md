---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b5eb671be022a6c3aa22e66f68386691fe23b275
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767334"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="93514-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="93514-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="93514-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93514-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93514-105">Recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="93514-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="93514-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="93514-106">Parameters</span></span>

 <span data-ttu-id="93514-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="93514-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="93514-108">[out] Ponteiro para um ponteiro para a estrutura de [SSortOrderSet](ssortorderset.md) mantendo a ordem de classificação atual.</span><span class="sxs-lookup"><span data-stu-id="93514-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="93514-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="93514-109">Return value</span></span>

<span data-ttu-id="93514-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="93514-110">S_OK</span></span> 
  
> <span data-ttu-id="93514-111">A ordem de classificação atual foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="93514-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="93514-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="93514-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="93514-113">Outra operação está em andamento que impede que a operação de recuperação de ordem de classificação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="93514-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="93514-114">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="93514-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93514-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="93514-115">Remarks</span></span>

<span data-ttu-id="93514-116">O método **IMAPITable::QuerySortOrder** recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="93514-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="93514-117">Ordens de classificação são descritas com uma estrutura [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="93514-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="93514-118">O membro **cSorts** da estrutura **SSortOrderSet** pode ser definido como zero se:</span><span class="sxs-lookup"><span data-stu-id="93514-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="93514-119">A tabela está sem classificação.</span><span class="sxs-lookup"><span data-stu-id="93514-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="93514-120">Não há nenhuma informação sobre como a tabela é classificada.</span><span class="sxs-lookup"><span data-stu-id="93514-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="93514-121">A estrutura de **SSortOrderSet** não é apropriada para descrever a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="93514-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="93514-122">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="93514-122">Notes to implementers</span></span>

<span data-ttu-id="93514-123">Se uma chamada for feita para o seu método [IMAPITable:: SortTable](imapitable-sorttable.md) com uma estrutura **SSortOrderSet** contendo zero colunas na chave de classificação, remova a ordem de classificação atual e aplicar a ordem padrão, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="93514-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="93514-124">Em chamadas subsequentes para **QuerySortOrder**, você pode escolher se deseja retornar zero ou mais colunas para a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="93514-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="93514-125">Você pode retornar mais colunas que estão no modo de exibição presente.</span><span class="sxs-lookup"><span data-stu-id="93514-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="93514-126">Para obter mais informações sobre a classificação, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="93514-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93514-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="93514-127">See also</span></span>



[<span data-ttu-id="93514-128">IMAPITable:: SortTable</span><span class="sxs-lookup"><span data-stu-id="93514-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="93514-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="93514-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="93514-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="93514-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="93514-131">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="93514-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


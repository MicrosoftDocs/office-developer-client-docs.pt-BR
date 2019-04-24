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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328858"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="931ee-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="931ee-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="931ee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="931ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="931ee-105">Recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="931ee-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="931ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="931ee-106">Parameters</span></span>

 <span data-ttu-id="931ee-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="931ee-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="931ee-108">bota Ponteiro para um ponteiro para a estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação atual.</span><span class="sxs-lookup"><span data-stu-id="931ee-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="931ee-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="931ee-109">Return value</span></span>

<span data-ttu-id="931ee-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="931ee-110">S_OK</span></span> 
  
> <span data-ttu-id="931ee-111">A ordem de classificação atual foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="931ee-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="931ee-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="931ee-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="931ee-113">Outra operação está em andamento, o que impede a inicialização da operação de recuperação da ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="931ee-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="931ee-114">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="931ee-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="931ee-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="931ee-115">Remarks</span></span>

<span data-ttu-id="931ee-116">O método imApitable **:: QuerySortOrder** recupera a ordem de classificação atual para uma tabela.</span><span class="sxs-lookup"><span data-stu-id="931ee-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="931ee-117">As ordens de classificação são descritas com uma estrutura [SSortOrderSet](ssortorderset.md) .</span><span class="sxs-lookup"><span data-stu-id="931ee-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="931ee-118">O membro **cSorts** da estrutura **SSortOrderSet** pode ser definido como zero se:</span><span class="sxs-lookup"><span data-stu-id="931ee-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="931ee-119">A tabela não está classificada.</span><span class="sxs-lookup"><span data-stu-id="931ee-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="931ee-120">Não há informações sobre como a tabela é classificada.</span><span class="sxs-lookup"><span data-stu-id="931ee-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="931ee-121">A estrutura **SSortOrderSet** não é adequada para descrever a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="931ee-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="931ee-122">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="931ee-122">Notes to implementers</span></span>

<span data-ttu-id="931ee-123">Se for feita uma chamada para o método imApitable [:: SortTable](imapitable-sorttable.md) com uma estrutura **SSortOrderSet** que contenha zero colunas na chave de classificação, remova a ordem de classificação atual e aplique a ordem padrão, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="931ee-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="931ee-124">Em chamadas subsequentes para **QuerySortOrder**, você pode escolher se deseja retornar zero ou mais colunas para a chave de classificação.</span><span class="sxs-lookup"><span data-stu-id="931ee-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="931ee-125">Você pode retornar mais colunas do que no modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="931ee-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="931ee-126">Para obter mais informações sobre classificação, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="931ee-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="931ee-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="931ee-127">See also</span></span>



[<span data-ttu-id="931ee-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="931ee-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="931ee-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="931ee-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="931ee-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="931ee-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="931ee-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="931ee-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


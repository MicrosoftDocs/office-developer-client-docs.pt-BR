---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767325"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="ec293-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ec293-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="ec293-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec293-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec293-105">Recolhe uma categoria de tabela expandida, removendo qualquer títulos de nível inferior e linhas da folha que pertencem à categoria da visualização de tabela.</span><span class="sxs-lookup"><span data-stu-id="ec293-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="ec293-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ec293-106">Parameters</span></span>

 <span data-ttu-id="ec293-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ec293-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="ec293-108">[in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="ec293-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="ec293-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ec293-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="ec293-110">[in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria.</span><span class="sxs-lookup"><span data-stu-id="ec293-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="ec293-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec293-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ec293-112">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ec293-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ec293-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="ec293-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="ec293-114">[out] Um ponteiro para o número total de linhas que estão sendo removidos do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="ec293-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec293-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ec293-115">Return value</span></span>

<span data-ttu-id="ec293-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec293-116">S_OK</span></span> 
  
> <span data-ttu-id="ec293-117">A operação de recolher teve êxito.</span><span class="sxs-lookup"><span data-stu-id="ec293-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="ec293-118">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ec293-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ec293-119">A linha identificada pelo parâmetro _pbInstanceKey_ não existe.</span><span class="sxs-lookup"><span data-stu-id="ec293-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="ec293-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ec293-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="ec293-121">A linha identificada pelo parâmetro _pbInstanceKey_ não existe.</span><span class="sxs-lookup"><span data-stu-id="ec293-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="ec293-122">Esse erro é uma alternativa ao E_NOT_FOUND; provedores de serviços podem retornar qualquer deles.</span><span class="sxs-lookup"><span data-stu-id="ec293-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ec293-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ec293-123">Remarks</span></span>

<span data-ttu-id="ec293-124">O método **IMAPITable::CollapseRow** recolhe uma categoria de tabela e a remove do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="ec293-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="ec293-125">As linhas são contraídas começando na linha identificada pela propriedade **PR_INSTANCE_KEY** apontada pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="ec293-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="ec293-126">O número de linhas que foram removidos do modo de exibição é retornado no conteúdo do parâmetro _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="ec293-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="ec293-127">Notificações nunca são geradas para as linhas de tabela que são removidas de um modo de exibição como resultado de uma operação de recolher.</span><span class="sxs-lookup"><span data-stu-id="ec293-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="ec293-128">Quando uma linha que é definida por um indicador é recolhida fora do modo de exibição, o indicador é movido para apontar para a próxima linha visível.</span><span class="sxs-lookup"><span data-stu-id="ec293-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="ec293-129">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="ec293-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec293-130">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ec293-130">MFCMAPI reference</span></span>

<span data-ttu-id="ec293-131">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec293-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec293-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ec293-132">**File**</span></span>|<span data-ttu-id="ec293-133">**Function**</span><span class="sxs-lookup"><span data-stu-id="ec293-133">**Function**</span></span>|<span data-ttu-id="ec293-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ec293-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec293-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ec293-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ec293-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="ec293-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="ec293-137">MFCMAPI usa o método **IMAPITable::CollapseRow** para recolher uma categoria de tabela.</span><span class="sxs-lookup"><span data-stu-id="ec293-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec293-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec293-138">See also</span></span>



[<span data-ttu-id="ec293-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ec293-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="ec293-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ec293-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="ec293-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ec293-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ec293-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="ec293-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="ec293-143">IMAPITable:: SortTable</span><span class="sxs-lookup"><span data-stu-id="ec293-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="ec293-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ec293-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="ec293-145">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec293-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ec293-146">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ec293-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


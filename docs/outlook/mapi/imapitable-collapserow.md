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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328951"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="402df-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="402df-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="402df-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="402df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="402df-105">Recolhe uma categoria de tabela expandida, removendo quaisquer títulos de nível inferior e linhas de folha pertencentes à categoria do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="402df-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="402df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="402df-106">Parameters</span></span>

 <span data-ttu-id="402df-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="402df-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="402df-108">no A contagem de bytes na propriedade PR_INSTANCE_KEY indicada pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="402df-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="402df-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="402df-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="402df-110">no Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria.</span><span class="sxs-lookup"><span data-stu-id="402df-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="402df-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="402df-111">_ulFlags_</span></span>
  
> <span data-ttu-id="402df-112">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="402df-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="402df-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="402df-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="402df-114">bota Um ponteiro para o número total de linhas que estão sendo removidas do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="402df-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="402df-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="402df-115">Return value</span></span>

<span data-ttu-id="402df-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="402df-116">S_OK</span></span> 
  
> <span data-ttu-id="402df-117">A operação de recolhimento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="402df-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="402df-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="402df-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="402df-119">A linha identificada pelo parâmetro _pbInstanceKey_ não existe.</span><span class="sxs-lookup"><span data-stu-id="402df-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="402df-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="402df-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="402df-121">A linha identificada pelo parâmetro _pbInstanceKey_ não existe.</span><span class="sxs-lookup"><span data-stu-id="402df-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="402df-122">Este erro é uma alternativa ao MAPI_E_NOT_FOUND; os provedores de serviços podem retornar um.</span><span class="sxs-lookup"><span data-stu-id="402df-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="402df-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="402df-123">Remarks</span></span>

<span data-ttu-id="402df-124">O método imApitable **:: CollapseRow** recolhe uma categoria de tabela e a remove da exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="402df-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="402df-125">As linhas são recolhidas começando pela linha identificada pela propriedade **PR_INSTANCE_KEY** indicada pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="402df-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="402df-126">O número de linhas que são removidas do modo de exibição é retornado no conteúdo do parâmetro _lpulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="402df-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="402df-127">As notificações nunca são geradas para linhas de tabela que são removidas de um modo de exibição como resultado de uma operação de recolhimento.</span><span class="sxs-lookup"><span data-stu-id="402df-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="402df-128">Quando uma linha definida por um indicador é recolhida da exibição, o indicador é movido para apontar para a próxima linha visível.</span><span class="sxs-lookup"><span data-stu-id="402df-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="402df-129">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="402df-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="402df-130">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="402df-130">MFCMAPI reference</span></span>

<span data-ttu-id="402df-131">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="402df-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="402df-132">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="402df-132">**File**</span></span>|<span data-ttu-id="402df-133">**Função**</span><span class="sxs-lookup"><span data-stu-id="402df-133">**Function**</span></span>|<span data-ttu-id="402df-134">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="402df-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="402df-135">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="402df-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="402df-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="402df-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="402df-137">MFCMAPI usa o método imApitable **:: CollapseRow** para recolher uma categoria de tabela.</span><span class="sxs-lookup"><span data-stu-id="402df-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="402df-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="402df-138">See also</span></span>



[<span data-ttu-id="402df-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="402df-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="402df-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="402df-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="402df-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="402df-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="402df-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="402df-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="402df-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="402df-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="402df-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="402df-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="402df-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="402df-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="402df-146">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="402df-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


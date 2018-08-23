---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ce78c6873f3a1dc034ae33f3c9e965ef8f2f1815
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563776"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="de7eb-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="de7eb-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="de7eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de7eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de7eb-105">Expande uma categoria de tabela recolhida, adicionando a folha ou linhas de cabeçalho de nível inferior que pertencem à categoria para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="de7eb-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="de7eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de7eb-106">Parameters</span></span>

 <span data-ttu-id="de7eb-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="de7eb-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="de7eb-108">[in] A contagem de bytes na propriedade PR_INSTANCE_KEY apontado pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="de7eb-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="de7eb-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="de7eb-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="de7eb-110">[in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) que identifica a linha de título para a categoria.</span><span class="sxs-lookup"><span data-stu-id="de7eb-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="de7eb-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="de7eb-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="de7eb-112">[in] O número máximo de linhas a serem retornadas no parâmetro _lppRows_ .</span><span class="sxs-lookup"><span data-stu-id="de7eb-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="de7eb-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de7eb-113">_ulFlags_</span></span>
  
> <span data-ttu-id="de7eb-114">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="de7eb-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="de7eb-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="de7eb-115">_lppRows_</span></span>
  
> <span data-ttu-id="de7eb-116">[out] Um ponteiro para uma estrutura [SRowSet](srowset.md) recebendo as linhas primeira (até _ulRowCount_) que foram inseridas em um modo de exibição de tabela como resultado da expansão.</span><span class="sxs-lookup"><span data-stu-id="de7eb-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="de7eb-117">Essas linhas são inseridas após a linha de título identificada pelo parâmetro _pbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="de7eb-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="de7eb-118">O parâmetro _lppRows_ pode ser NULL se o parâmetro _ulRowCount_ for zero.</span><span class="sxs-lookup"><span data-stu-id="de7eb-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="de7eb-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="de7eb-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="de7eb-120">[out] Um ponteiro para o número total de linhas que foram adicionados ao modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="de7eb-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de7eb-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="de7eb-121">Return value</span></span>

<span data-ttu-id="de7eb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="de7eb-122">S_OK</span></span> 
  
> <span data-ttu-id="de7eb-123">A categoria foi expandida com êxito.</span><span class="sxs-lookup"><span data-stu-id="de7eb-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="de7eb-124">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="de7eb-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="de7eb-125">A linha identificada pelo parâmetro _pbInstanceKey_ não existe.</span><span class="sxs-lookup"><span data-stu-id="de7eb-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de7eb-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="de7eb-126">Remarks</span></span>

<span data-ttu-id="de7eb-127">O método **IMAPITable::ExpandRow** expande uma categoria de tabela recolhida, adicionando a folha ou linhas de cabeçalho de nível inferior que pertencem à categoria para o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="de7eb-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="de7eb-128">Um limite no número de linhas a serem retornados no parâmetro _lppRows_ pode ser especificado no parâmetro _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="de7eb-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="de7eb-129">Quando _ulRowCount_ estiver definida como um valor maior que zero e uma ou mais linhas são retornadas no conjunto de linha apontado pela _lppRows_, defina a posição do indicador que bookmark_current é movido para a linha imediatamente após a última linha a linha.</span><span class="sxs-lookup"><span data-stu-id="de7eb-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="de7eb-130">Quando _ulRowCount_ estiver definida como zero, solicitando que zero folha ou linhas de título de nível inferior adicionadas à categoria ou zero linhas são retornadas porque não há nenhuma folha ou linhas de cabeçalho de nível inferior na categoria, a posição do BOOKMARK_CURRENT é definida como a linha seguindo a linha identificada pela _pbInstanceKey_.</span><span class="sxs-lookup"><span data-stu-id="de7eb-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="de7eb-131">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="de7eb-131">Notes to implementers</span></span>

<span data-ttu-id="de7eb-132">Sem gere notificações em linhas que são adicionadas a um modo de exibição de tabela devido à expansão de categoria.</span><span class="sxs-lookup"><span data-stu-id="de7eb-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="de7eb-133">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="de7eb-133">Notes to callers</span></span>

<span data-ttu-id="de7eb-134">O número de linhas no conjunto de linha apontado pelo parâmetro _lppRows_ não pode ser igual ao número de linhas que realmente foram adicionados à tabela, todo o conjunto de folha ou heading linhas para a categoria de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="de7eb-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="de7eb-135">Podem ocorrer erros, como memória insuficiente ou o número de linhas na categoria exceder o número especificado no parâmetro _ulRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="de7eb-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="de7eb-136">Em ambos os casos, BOOKMARK_CURRENT será posicionada na última linha retornada.</span><span class="sxs-lookup"><span data-stu-id="de7eb-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="de7eb-137">Para recuperar imediatamente o restante das linhas da categoria, chame [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="de7eb-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="de7eb-138">Não espera receber uma notificação de tabela quando seu estado de mudar de uma categoria.</span><span class="sxs-lookup"><span data-stu-id="de7eb-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="de7eb-139">Você pode manter um cache local de linhas que podem ser atualizados com cada chamada **ExpandRow** ou **CollapseRow** .</span><span class="sxs-lookup"><span data-stu-id="de7eb-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="de7eb-140">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="de7eb-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="de7eb-141">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="de7eb-141">MFCMAPI reference</span></span>

<span data-ttu-id="de7eb-142">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="de7eb-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="de7eb-143">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="de7eb-143">**File**</span></span>|<span data-ttu-id="de7eb-144">**Function**</span><span class="sxs-lookup"><span data-stu-id="de7eb-144">**Function**</span></span>|<span data-ttu-id="de7eb-145">**Comment**</span><span class="sxs-lookup"><span data-stu-id="de7eb-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de7eb-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="de7eb-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="de7eb-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="de7eb-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="de7eb-148">MFCMAPI usa o método **IMAPITable::ExpandRow** para expandir uma categoria de tabela recolhida.</span><span class="sxs-lookup"><span data-stu-id="de7eb-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de7eb-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="de7eb-149">See also</span></span>



[<span data-ttu-id="de7eb-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="de7eb-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="de7eb-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="de7eb-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="de7eb-152">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="de7eb-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


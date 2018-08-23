---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567899"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="fa28d-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="fa28d-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="fa28d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa28d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa28d-105">Recriará o estado atual de expandidos ou recolhido de uma tabela categorizado usando os dados que foi salvo por uma chamada anterior para o método [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa28d-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="fa28d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa28d-106">Parameters</span></span>

 <span data-ttu-id="fa28d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa28d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fa28d-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fa28d-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fa28d-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="fa28d-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="fa28d-110">[in] Contagem de bytes na estrutura apontado pelo parâmetro _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="fa28d-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="fa28d-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="fa28d-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="fa28d-112">[in] Ponteiro para as estruturas contendo os dados necessários para recriar o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="fa28d-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="fa28d-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="fa28d-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="fa28d-114">[out] Ponteiro para um indicador que identifica a linha da tabela na qual o estado recolhido ou expandido deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="fa28d-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="fa28d-115">Este indicador e a chave de instância passada no parâmetro _lpbInstanceKey_ na chamada a [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identificam a mesma linha.</span><span class="sxs-lookup"><span data-stu-id="fa28d-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa28d-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fa28d-116">Return value</span></span>

<span data-ttu-id="fa28d-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa28d-117">S_OK</span></span> 
  
> <span data-ttu-id="fa28d-118">O estado da tabela categorizado foi reconstruído com êxito.</span><span class="sxs-lookup"><span data-stu-id="fa28d-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="fa28d-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="fa28d-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="fa28d-120">Outra operação está em andamento que impede que a operação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="fa28d-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="fa28d-121">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="fa28d-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="fa28d-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="fa28d-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="fa28d-123">A tabela não pôde concluir a recriação o modo de exibição recolhido ou expandido.</span><span class="sxs-lookup"><span data-stu-id="fa28d-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa28d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa28d-124">Remarks</span></span>

<span data-ttu-id="fa28d-125">O método **IMAPITable::SetCollapseState** restabelece o estado expandido ou recolhido do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="fa28d-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="fa28d-126">**SetCollapseState** e **GetCollapseState** funcionam juntas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fa28d-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="fa28d-127">Quando o estado de uma tabela categorizado está prestes a ser alterada, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) é chamado para salvar todos os dados referentes ao estado anterior a alteração.</span><span class="sxs-lookup"><span data-stu-id="fa28d-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="fa28d-128">Para restaurar o modo de exibição da tabela ao seu estado salvo, **SetCollapseState** é chamado.</span><span class="sxs-lookup"><span data-stu-id="fa28d-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="fa28d-129">Os dados salvos pelo **GetCollapseState** são passados para **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="fa28d-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="fa28d-130">**SetCollapseState** é capaz de usar esses dados para restaurar o estado.</span><span class="sxs-lookup"><span data-stu-id="fa28d-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="fa28d-131">**SetCollapseState** retorna um indicador que identifica a mesma linha como a chave de instância passada como entrada para **GetCollapseState**como um parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="fa28d-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="fa28d-132">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="fa28d-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fa28d-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="fa28d-133">Notes to implementers</span></span>

<span data-ttu-id="fa28d-134">Você é responsável por verificar que a ordem de classificação e restrições forem exatamente iguais como estavam no momento da chamada **GetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="fa28d-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="fa28d-135">Se uma alteração foi feita, **SetCollapseState** não deve ser chamado porque os resultados podem ser imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="fa28d-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="fa28d-136">Isso pode acontecer se, por exemplo, um cliente chama **GetCollapseState** e **SortTable** para alterar a chave de classificação antes de chamar **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="fa28d-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="fa28d-137">Para estar seguro, verifique se os dados salvos ainda são válidos antes de prosseguir com a restauração.</span><span class="sxs-lookup"><span data-stu-id="fa28d-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa28d-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="fa28d-138">Notes to callers</span></span>

<span data-ttu-id="fa28d-139">Para chamar **SetCollapseState**, você anteriormente deve ter chamado **GetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="fa28d-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="fa28d-140">A ordem de classificação estabelecer as categorias deve ser o mesmo para os dois métodos.</span><span class="sxs-lookup"><span data-stu-id="fa28d-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="fa28d-141">Se as ordens de classificação forem diferentes, os resultados da operação **SetCollapseState** serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="fa28d-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa28d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa28d-142">See also</span></span>



[<span data-ttu-id="fa28d-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="fa28d-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="fa28d-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="fa28d-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="fa28d-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="fa28d-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="fa28d-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa28d-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


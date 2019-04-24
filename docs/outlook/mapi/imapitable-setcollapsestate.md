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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328830"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="9b7c0-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9b7c0-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="9b7c0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b7c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b7c0-105">Recria o estado atual expandido ou recolhido de uma tabela categorizada usando dados que foram salvos por uma chamada anterior para o método [IMAPITable::](imapitable-getcollapsestate.md) getcollapsestate.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="9b7c0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b7c0-106">Parameters</span></span>

 <span data-ttu-id="9b7c0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b7c0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9b7c0-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9b7c0-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9b7c0-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="9b7c0-110">no Contagem de bytes na estrutura apontada pelo parâmetro _pbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="9b7c0-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="9b7c0-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9b7c0-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="9b7c0-112">no Ponteiro para as estruturas que contêm os dados necessários para reconstruir o modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="9b7c0-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="9b7c0-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="9b7c0-114">bota Ponteiro para um indicador identificando a linha na tabela na qual o estado recolhido ou expandido deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="9b7c0-115">Este indicador e a chave de instância passada no parâmetro _lpbInstanceKey_ na chamada para IMAPITable [::](imapitable-getcollapsestate.md) getcollapsestate identificam a mesma linha.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9b7c0-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9b7c0-116">Return value</span></span>

<span data-ttu-id="9b7c0-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b7c0-117">S_OK</span></span> 
  
> <span data-ttu-id="9b7c0-118">O estado da tabela categorizada foi reconstruído com êxito.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="9b7c0-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9b7c0-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9b7c0-120">Outra operação está em andamento, o que impede a inicialização da operação.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="9b7c0-121">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="9b7c0-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="9b7c0-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="9b7c0-123">A tabela não pôde concluir a reconstrução da exibição recolhida ou expandida.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b7c0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b7c0-124">Remarks</span></span>

<span data-ttu-id="9b7c0-125">O método imApitable **::** setcollapsestate restabelece o estado expandido ou recolhido do modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="9b7c0-126">\*\*\*\* Setcollapsestate e \*\*\*\* getcollapsestate funcionam juntos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9b7c0-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="9b7c0-127">Quando o estado de uma tabela categorizada está prestes a mudar, [IMAPITable::](imapitable-getcollapsestate.md) getcollapsestate é chamado para salvar todos os dados pertencentes ao estado anterior à alteração.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="9b7c0-128">Para restaurar o modo de exibição da tabela para seu estado salvo \*\*\*\* , setcollapsestate é chamado.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="9b7c0-129">Os dados salvos por \*\*\*\* getcollapsestate são passados para \*\*\*\* setcollapsestate.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="9b7c0-130">\*\*\*\* Setcollapsestate é capaz de usar esses dados para restaurar o estado.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="9b7c0-131">\*\*\*\* Setcollapsestate retorna como um parâmetro de saída um indicador que identifica a mesma linha que a chave de instância passada como entrada para getcollapsestate. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b7c0-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="9b7c0-132">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="9b7c0-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9b7c0-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="9b7c0-133">Notes to implementers</span></span>

<span data-ttu-id="9b7c0-134">Você é responsável por verificar se a ordem de classificação e as restrições são exatamente iguais às que foram no momento da chamada getCollapsestate. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b7c0-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="9b7c0-135">Se uma alteração tiver sido feita, \*\*\*\* setcollapsestate não deverá ser chamado porque os resultados podem ser imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="9b7c0-136">Isso pode acontecer se, por exemplo, um cliente chama \*\*\*\* getcollapsestate e **SortTable** para alterar a chave de classificação antes de \*\*\*\* chamar setcollapsestate.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="9b7c0-137">Para ser seguro, verifique se os dados salvos ainda são válidos antes de prosseguir com a restauração.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b7c0-138">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9b7c0-138">Notes to callers</span></span>

<span data-ttu-id="9b7c0-139">Para chamar \*\*\*\* setcollapsestate, você deve ter chamado getcollapsestate anteriormente. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b7c0-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="9b7c0-140">A ordem de classificação que estabelece as categorias deve ser a mesma para os dois métodos.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="9b7c0-141">Se as ordens de classificação forem diferentes, os resultados \*\*\*\* da operação setcollapsestate serão imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="9b7c0-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b7c0-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b7c0-142">See also</span></span>



[<span data-ttu-id="9b7c0-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="9b7c0-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="9b7c0-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="9b7c0-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="9b7c0-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9b7c0-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="9b7c0-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b7c0-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


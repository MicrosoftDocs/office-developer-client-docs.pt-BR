---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589662"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="42ac9-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="42ac9-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="42ac9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42ac9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42ac9-105">Retorna os dados que não é necessário para reconstruir atual recolhido ou expandido o estado de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="42ac9-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="42ac9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42ac9-106">Parameters</span></span>

 <span data-ttu-id="42ac9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="42ac9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="42ac9-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="42ac9-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="42ac9-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="42ac9-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="42ac9-110">[in] A contagem de bytes na chave instância apontado pelo parâmetro _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="42ac9-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="42ac9-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="42ac9-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="42ac9-112">[in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha no qual as atuais recolhido ou expandida estado deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="42ac9-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="42ac9-113">O parâmetro _lpbInstanceKey_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="42ac9-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="42ac9-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="42ac9-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="42ac9-115">[out] Um ponteiro para a contagem de estruturas apontado pelo parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="42ac9-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="42ac9-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="42ac9-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="42ac9-117">[out] Um ponteiro para um ponteiro para estruturas que contenham dados que descreve o modo de exibição de tabela atual.</span><span class="sxs-lookup"><span data-stu-id="42ac9-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="42ac9-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="42ac9-118">Return value</span></span>

<span data-ttu-id="42ac9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="42ac9-119">S_OK</span></span> 
  
> <span data-ttu-id="42ac9-120">O estado da tabela categorizado foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="42ac9-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="42ac9-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="42ac9-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="42ac9-122">Outra operação está em andamento que impede que a operação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="42ac9-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="42ac9-123">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="42ac9-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="42ac9-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="42ac9-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="42ac9-125">A tabela não oferece suporte a categorização e exibições expandida e recolhida.</span><span class="sxs-lookup"><span data-stu-id="42ac9-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="42ac9-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="42ac9-126">Remarks</span></span>

<span data-ttu-id="42ac9-127">O método **IMAPITable::GetCollapseState** funciona com o método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para alterar o modo de exibição do usuário de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="42ac9-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="42ac9-128">**GetCollapseState** salva os dados que é necessário para **SetCollapseState** será usado para reconstruir os modos de exibição apropriados das categorias de uma tabela categorizada.</span><span class="sxs-lookup"><span data-stu-id="42ac9-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="42ac9-129">Provedores de serviços de determinam os dados a serem salvos.</span><span class="sxs-lookup"><span data-stu-id="42ac9-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="42ac9-130">No entanto, a maioria dos provedores de serviço implementando **GetCollapseState** salvar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="42ac9-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="42ac9-131">As chaves de classificação (standard colunas e colunas de categoria).</span><span class="sxs-lookup"><span data-stu-id="42ac9-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="42ac9-132">Informações sobre a linha que representa a chave da instância.</span><span class="sxs-lookup"><span data-stu-id="42ac9-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="42ac9-133">Informações para restaurar as categorias expandidas e recolhidas da tabela.</span><span class="sxs-lookup"><span data-stu-id="42ac9-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="42ac9-134">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="42ac9-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="42ac9-135">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="42ac9-135">Notes to implementers</span></span>

<span data-ttu-id="42ac9-136">Armazene o estado atual de todos os nós de uma tabela no parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="42ac9-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="42ac9-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="42ac9-137">Notes to callers</span></span>

<span data-ttu-id="42ac9-138">Sempre chame **GetCollapseState** antes de chamar **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="42ac9-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42ac9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="42ac9-139">See also</span></span>



[<span data-ttu-id="42ac9-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="42ac9-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="42ac9-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42ac9-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


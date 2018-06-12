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
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767321"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="73260-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="73260-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="73260-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="73260-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="73260-105">Retorna os dados que não é necessário para reconstruir atual recolhido ou expandido o estado de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="73260-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="73260-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="73260-106">Parameters</span></span>

 <span data-ttu-id="73260-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73260-107">_ulFlags_</span></span>
  
> <span data-ttu-id="73260-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="73260-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="73260-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="73260-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="73260-110">[in] A contagem de bytes na chave instância apontado pelo parâmetro _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="73260-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="73260-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="73260-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="73260-112">[in] Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha no qual as atuais recolhido ou expandida estado deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="73260-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="73260-113">O parâmetro _lpbInstanceKey_ não pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="73260-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="73260-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="73260-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="73260-115">[out] Um ponteiro para a contagem de estruturas apontado pelo parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="73260-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="73260-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="73260-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="73260-117">[out] Um ponteiro para um ponteiro para estruturas que contenham dados que descreve o modo de exibição de tabela atual.</span><span class="sxs-lookup"><span data-stu-id="73260-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73260-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="73260-118">Return value</span></span>

<span data-ttu-id="73260-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="73260-119">S_OK</span></span> 
  
> <span data-ttu-id="73260-120">O estado da tabela categorizado foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="73260-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="73260-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="73260-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="73260-122">Outra operação está em andamento que impede que a operação seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="73260-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="73260-123">Ou a operação em andamento deve ter permissão para concluir ou ele deve ser interrompido.</span><span class="sxs-lookup"><span data-stu-id="73260-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="73260-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="73260-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="73260-125">A tabela não oferece suporte a categorização e exibições expandida e recolhida.</span><span class="sxs-lookup"><span data-stu-id="73260-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73260-126">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="73260-126">Remarks</span></span>

<span data-ttu-id="73260-127">O método **IMAPITable::GetCollapseState** funciona com o método [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) para alterar o modo de exibição do usuário de uma tabela categorizado.</span><span class="sxs-lookup"><span data-stu-id="73260-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="73260-128">**GetCollapseState** salva os dados que é necessário para **SetCollapseState** será usado para reconstruir os modos de exibição apropriados das categorias de uma tabela categorizada.</span><span class="sxs-lookup"><span data-stu-id="73260-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="73260-129">Provedores de serviços de determinam os dados a serem salvos.</span><span class="sxs-lookup"><span data-stu-id="73260-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="73260-130">No entanto, a maioria dos provedores de serviço implementando **GetCollapseState** salvar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="73260-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="73260-131">As chaves de classificação (standard colunas e colunas de categoria).</span><span class="sxs-lookup"><span data-stu-id="73260-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="73260-132">Informações sobre a linha que representa a chave da instância.</span><span class="sxs-lookup"><span data-stu-id="73260-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="73260-133">Informações para restaurar as categorias expandidas e recolhidas da tabela.</span><span class="sxs-lookup"><span data-stu-id="73260-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="73260-134">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="73260-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73260-135">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="73260-135">Notes to implementers</span></span>

<span data-ttu-id="73260-136">Armazene o estado atual de todos os nós de uma tabela no parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="73260-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73260-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="73260-137">Notes to callers</span></span>

<span data-ttu-id="73260-138">Sempre chame **GetCollapseState** antes de chamar **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="73260-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73260-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="73260-139">See also</span></span>



[<span data-ttu-id="73260-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="73260-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="73260-141">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="73260-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


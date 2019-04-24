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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328922"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="73fb7-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="73fb7-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="73fb7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73fb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73fb7-105">Retorna os dados necessários para reconstruir o estado atual recolhido ou expandido de uma tabela categorizada.</span><span class="sxs-lookup"><span data-stu-id="73fb7-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="73fb7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73fb7-106">Parameters</span></span>

 <span data-ttu-id="73fb7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="73fb7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="73fb7-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="73fb7-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="73fb7-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="73fb7-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="73fb7-110">no A contagem de bytes na chave de instância indicada pelo parâmetro _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="73fb7-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="73fb7-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="73fb7-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="73fb7-112">no Um ponteiro para a propriedade **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) da linha na qual o estado atual recolhido ou expandido deve ser recriado.</span><span class="sxs-lookup"><span data-stu-id="73fb7-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="73fb7-113">O parâmetro _lpbInstanceKey_ não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="73fb7-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="73fb7-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="73fb7-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="73fb7-115">bota Um ponteiro para a contagem de estruturas apontada pelo parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="73fb7-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="73fb7-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="73fb7-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="73fb7-117">bota Um ponteiro para um ponteiro para estruturas que contêm dados que descrevem o modo de exibição de tabela atual.</span><span class="sxs-lookup"><span data-stu-id="73fb7-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="73fb7-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="73fb7-118">Return value</span></span>

<span data-ttu-id="73fb7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="73fb7-119">S_OK</span></span> 
  
> <span data-ttu-id="73fb7-120">O estado da tabela categorizada foi salvo com êxito.</span><span class="sxs-lookup"><span data-stu-id="73fb7-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="73fb7-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="73fb7-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="73fb7-122">Outra operação está em andamento, o que impede a inicialização da operação.</span><span class="sxs-lookup"><span data-stu-id="73fb7-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="73fb7-123">A operação em andamento deve ter permissão para ser concluída ou deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="73fb7-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="73fb7-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="73fb7-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="73fb7-125">A tabela não dá suporte a categorização e exibições expandidas e recolhidas.</span><span class="sxs-lookup"><span data-stu-id="73fb7-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="73fb7-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="73fb7-126">Remarks</span></span>

<span data-ttu-id="73fb7-127">O método imApitable **::** getcollapsestate funciona com o método IMAPITable [::](imapitable-setcollapsestate.md) setcollapsestate para alterar o modo de exibição do usuário de uma tabela categorizada.</span><span class="sxs-lookup"><span data-stu-id="73fb7-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="73fb7-128">\*\*\*\* Getcollapsestate salva os dados necessários para setcollapsestate a ser usado para reconstruir as exibições apropriadas das categorias de uma tabela categorizada. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="73fb7-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="73fb7-129">Os provedores de serviços determinam os dados a serem salvos.</span><span class="sxs-lookup"><span data-stu-id="73fb7-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="73fb7-130">No enTanto, a maioria \*\*\*\* dos provedores de serviços que implementam getcollapsestate salvam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="73fb7-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="73fb7-131">As chaves de classificação (colunas de categoria e colunas padrão).</span><span class="sxs-lookup"><span data-stu-id="73fb7-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="73fb7-132">Informações sobre a linha que a chave de instância representa.</span><span class="sxs-lookup"><span data-stu-id="73fb7-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="73fb7-133">Informações para restaurar as categorias recolhidas e expandidas da tabela.</span><span class="sxs-lookup"><span data-stu-id="73fb7-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="73fb7-134">Para obter mais informações sobre tabelas categorizadas, consulte [classificação e categorização](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="73fb7-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="73fb7-135">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="73fb7-135">Notes to implementers</span></span>

<span data-ttu-id="73fb7-136">Armazenar o estado atual de todos os nós de uma tabela no parâmetro _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="73fb7-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="73fb7-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="73fb7-137">Notes to callers</span></span>

<span data-ttu-id="73fb7-138">Chame sempre \*\*\*\* getcollapsestate antes de chamar \*\*\*\* setcollapsestate.</span><span class="sxs-lookup"><span data-stu-id="73fb7-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="73fb7-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="73fb7-139">See also</span></span>



[<span data-ttu-id="73fb7-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="73fb7-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="73fb7-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="73fb7-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


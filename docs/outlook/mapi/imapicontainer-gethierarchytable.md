---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426195"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="e1413-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="e1413-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="e1413-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1413-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1413-105">Retorna um ponteiro para a tabela de hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1413-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e1413-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1413-106">Parameters</span></span>

 <span data-ttu-id="e1413-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e1413-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e1413-108">[in] Uma máscara de bits de sinalizadores que controla como as informações são retornadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="e1413-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="e1413-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e1413-109">The following flags can be set:</span></span>
    
<span data-ttu-id="e1413-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="e1413-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="e1413-111">Preenche a tabela de hierarquia com contêineres de vários níveis.</span><span class="sxs-lookup"><span data-stu-id="e1413-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="e1413-112">Se CONVENIENT_DEPTH não estiver definida, a tabela de hierarquias conterá apenas os contêineres filho imediatos do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1413-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="e1413-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e1413-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e1413-114">**GetHierarchyTable** pode retornar com êxito, possivelmente antes da tabela ser disponibilizada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="e1413-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="e1413-115">Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá criar um erro.</span><span class="sxs-lookup"><span data-stu-id="e1413-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="e1413-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e1413-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e1413-117">Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1413-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="e1413-118">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e1413-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="e1413-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="e1413-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="e1413-120">Mostra itens que estão marcados como excluídos de forma suave, ou seja, eles estão na fase de tempo de retenção de itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="e1413-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="e1413-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e1413-121">_lppTable_</span></span>
  
> <span data-ttu-id="e1413-122">[out] Um ponteiro para um ponteiro para a tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e1413-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e1413-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e1413-123">Return value</span></span>

<span data-ttu-id="e1413-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1413-124">S_OK</span></span> 
  
> <span data-ttu-id="e1413-125">A tabela de hierarquias foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="e1413-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="e1413-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e1413-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e1413-127">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="e1413-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="e1413-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e1413-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e1413-129">O contêiner não tem contêineres filhos e não pode fornecer uma tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e1413-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e1413-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1413-130">Remarks</span></span>

<span data-ttu-id="e1413-131">O **método IMAPIContainer::GetHierarchyTable** retorna um ponteiro para a tabela de hierarquia de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1413-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="e1413-132">Uma tabela de hierarquia contém informações resumidas sobre os contêineres filho no contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1413-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="e1413-133">As tabelas de hierarquia de pastas têm informações sobre subpastas; as tabelas de hierarquia do livro de endereços têm informações sobre contêineres do livro de endereços filho e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="e1413-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="e1413-134">É possível que alguns contêineres não tenham contêineres filhos.</span><span class="sxs-lookup"><span data-stu-id="e1413-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="e1413-135">Esses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="e1413-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="e1413-136">Quando o CONVENIENT_DEPTH de comando é definido, cada linha na tabela de hierarquia também inclui a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como uma coluna.</span><span class="sxs-lookup"><span data-stu-id="e1413-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="e1413-137">**PR_DEPTH** indica o nível de cada contêiner em relação ao contêiner que implementa a tabela.</span><span class="sxs-lookup"><span data-stu-id="e1413-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="e1413-138">Os contêineres filho imediatos do contêiner estão na profundidade zero, os contêineres filho nos contêineres de profundidade zero estão em profundidade um e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e1413-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="e1413-139">Os valores de **PR_DEPTH** aumentam sequencialmente à medida que a hierarquia de níveis se aprofunda.</span><span class="sxs-lookup"><span data-stu-id="e1413-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="e1413-140">Para uma lista completa de colunas necessárias e opcionais em tabelas de hierarquias, consulte [Tabelas de Hierarquia.](hierarchy-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e1413-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e1413-141">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="e1413-141">Notes to implementers</span></span>

<span data-ttu-id="e1413-142">Se você tiver suporte para uma tabela de hierarquia para seu contêiner, também deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e1413-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="e1413-143">Suporte a uma chamada para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1413-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="e1413-144">Retorne **PR_CONTAINER_HIERARCHY** de uma chamada para os métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e1413-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="e1413-145">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e1413-145">Notes to callers</span></span>

<span data-ttu-id="e1413-146">As colunas da tabela de cadeia de caracteres e conteúdo binário podem ser truncadas.</span><span class="sxs-lookup"><span data-stu-id="e1413-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="e1413-147">Normalmente, os provedores retornam 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e1413-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="e1413-148">Como não é possível saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna seja truncada se o tamanho da coluna for de 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="e1413-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="e1413-149">Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-la e, em seguida, chamando o método [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="e1413-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="e1413-150">Dependendo da implementação do provedor, as restrições e as operações de classificação podem ser aplicadas à cadeia de caracteres inteira ou à versão truncada dessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e1413-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="e1413-151">Além disso, os provedores de armazenamento não têm garantia de atender ao conjunto de ordem de classificação [SSortOrderSet](ssortorderset.md) especificado para tabelas de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="e1413-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e1413-152">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e1413-152">MFCMAPI reference</span></span>

<span data-ttu-id="e1413-153">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e1413-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e1413-154">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e1413-154">**File**</span></span>|<span data-ttu-id="e1413-155">**Função**</span><span class="sxs-lookup"><span data-stu-id="e1413-155">**Function**</span></span>|<span data-ttu-id="e1413-156">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="e1413-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1413-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e1413-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e1413-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="e1413-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="e1413-159">A classe CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obter tabelas de hierarquia para exibir em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="e1413-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1413-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1413-160">See also</span></span>



[<span data-ttu-id="e1413-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="e1413-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="e1413-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="e1413-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="e1413-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1413-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="e1413-164">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="e1413-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="e1413-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e1413-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="e1413-166">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e1413-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


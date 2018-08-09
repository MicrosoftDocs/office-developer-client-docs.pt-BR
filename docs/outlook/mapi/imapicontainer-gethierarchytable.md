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
ms.openlocfilehash: b30c6e9840ed5dddfd2d3a5f149a3f0f6e8da605
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766966"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="aece5-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="aece5-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="aece5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aece5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aece5-105">Retorna um ponteiro para a tabela de hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="aece5-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="aece5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aece5-106">Parameters</span></span>

 <span data-ttu-id="aece5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aece5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="aece5-108">[in] Uma bitmask dos sinalizadores que controla como as informações são retornadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="aece5-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="aece5-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="aece5-109">The following flags can be set:</span></span>
    
<span data-ttu-id="aece5-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="aece5-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="aece5-111">Preenche a tabela de hierarquia com contêineres de vários níveis.</span><span class="sxs-lookup"><span data-stu-id="aece5-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="aece5-112">Se CONVENIENT_DEPTH não estiver definida, a tabela de hierarquia contém apenas os contêineres de filho imediato do contêiner.</span><span class="sxs-lookup"><span data-stu-id="aece5-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="aece5-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="aece5-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="aece5-114">**GetHierarchyTable** pode retornar com êxito, possivelmente antes que a tabela é disponibilizada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="aece5-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="aece5-115">Se a tabela não estiver disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="aece5-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="aece5-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aece5-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="aece5-117">Solicitações que as colunas que contêm dados de cadeia de caracteres a ser retornado em formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="aece5-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="aece5-118">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem ser retornadas no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="aece5-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="aece5-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="aece5-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="aece5-120">Mostra os itens que estão marcados como suaves excluídos — ou seja, eles estão na retenção de item excluído fase de tempo.</span><span class="sxs-lookup"><span data-stu-id="aece5-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="aece5-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="aece5-121">_lppTable_</span></span>
  
> <span data-ttu-id="aece5-122">[out] Um ponteiro para um ponteiro para a tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="aece5-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aece5-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aece5-123">Return value</span></span>

<span data-ttu-id="aece5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="aece5-124">S_OK</span></span> 
  
> <span data-ttu-id="aece5-125">A tabela de hierarquia foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="aece5-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="aece5-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="aece5-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="aece5-127">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="aece5-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="aece5-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="aece5-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="aece5-129">O contêiner tem sem contêineres filho e não pode fornecer uma tabela de hierarquia.</span><span class="sxs-lookup"><span data-stu-id="aece5-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aece5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="aece5-130">Remarks</span></span>

<span data-ttu-id="aece5-131">O método **IMAPIContainer::GetHierarchyTable** retorna um ponteiro para a tabela de hierarquia de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="aece5-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="aece5-132">Uma tabela de hierarquia contém informações de resumo sobre os contêineres filho no contêiner.</span><span class="sxs-lookup"><span data-stu-id="aece5-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="aece5-133">Tabelas de hierarquias de pasta mantêm informações sobre subpastas; tabelas de hierarquias de catálogo de endereços mantêm informações sobre filho contêineres do catálogo de endereços e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="aece5-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="aece5-134">É possível que alguns contêineres ter sem contêineres filho.</span><span class="sxs-lookup"><span data-stu-id="aece5-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="aece5-135">Desses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="aece5-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="aece5-136">Quando o sinalizador CONVENIENT_DEPTH estiver definido, cada linha da tabela de hierarquia também inclui a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como uma coluna.</span><span class="sxs-lookup"><span data-stu-id="aece5-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="aece5-137">**PR_DEPTH** indica o nível de cada contêiner em relação ao contêiner que implementa a tabela.</span><span class="sxs-lookup"><span data-stu-id="aece5-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="aece5-138">Filho imediato de implementação do contêiner contêineres correm depth zero, recipientes filho nos contêineres de zero profundidade correm profundidade um e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="aece5-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="aece5-139">Os valores de **PR_DEPTH** aumentam sequencialmente à medida que aprofunda a hierarquia dos níveis.</span><span class="sxs-lookup"><span data-stu-id="aece5-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="aece5-140">Para obter uma lista completa das colunas obrigatórios e opcionais em tabelas de hierarquias, consulte as [Tabelas de hierarquias](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="aece5-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="aece5-141">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="aece5-141">Notes to implementers</span></span>

<span data-ttu-id="aece5-142">Caso você ofereça suporte a uma tabela de hierarquia de seu contêiner, você deve também faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="aece5-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="aece5-143">Suporte a uma chamada ao método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aece5-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="aece5-144">Retorne **PR_CONTAINER_HIERARCHY** de uma chamada para os métodos de [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner.</span><span class="sxs-lookup"><span data-stu-id="aece5-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="aece5-145">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="aece5-145">Notes to callers</span></span>

<span data-ttu-id="aece5-146">Cadeia de caracteres e binário colunas da tabela de conteúdo podem ser truncadas.</span><span class="sxs-lookup"><span data-stu-id="aece5-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="aece5-147">Normalmente, provedores retornam 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="aece5-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="aece5-148">Porque você não pode saber com antecedência se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna é 255 ou 510 bytes.</span><span class="sxs-lookup"><span data-stu-id="aece5-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="aece5-149">Você sempre pode recuperar o valor completo de uma coluna truncado, se necessário, diretamente do objeto utilizando seu identificador de entrada para abri-lo e, em seguida, chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="aece5-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="aece5-150">Dependendo da implementação do provedor, restrições e operações de classificação podem aplicar para a cadeia de caracteres inteira ou para a versão truncada da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="aece5-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="aece5-151">Além disso, provedores de armazenamento não há uma garantia honram o conjunto de ordem de classificação [que ssortorderset](ssortorderset.md) especificado para tabelas de hierarquias.</span><span class="sxs-lookup"><span data-stu-id="aece5-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aece5-152">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="aece5-152">MFCMAPI reference</span></span>

<span data-ttu-id="aece5-153">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="aece5-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aece5-154">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="aece5-154">**File**</span></span>|<span data-ttu-id="aece5-155">**Function**</span><span class="sxs-lookup"><span data-stu-id="aece5-155">**Function**</span></span>|<span data-ttu-id="aece5-156">**Comment**</span><span class="sxs-lookup"><span data-stu-id="aece5-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aece5-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="aece5-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="aece5-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="aece5-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="aece5-159">A classe CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obter as tabelas de hierarquias para exibir em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="aece5-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aece5-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="aece5-160">See also</span></span>



[<span data-ttu-id="aece5-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="aece5-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="aece5-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="aece5-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="aece5-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aece5-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="aece5-164">Propriedade canônica PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="aece5-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="aece5-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aece5-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="aece5-166">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="aece5-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


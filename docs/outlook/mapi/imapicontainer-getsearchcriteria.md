---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 13c151a134e4334e8ed2e75e031a6fc9dddbf941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766944"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="ceb45-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ceb45-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="ceb45-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ceb45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ceb45-105">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="ceb45-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="ceb45-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ceb45-106">Parameters</span></span>

 <span data-ttu-id="ceb45-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ceb45-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ceb45-108">[in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado.</span><span class="sxs-lookup"><span data-stu-id="ceb45-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="ceb45-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="ceb45-109">The following flag can be set:</span></span>
    
<span data-ttu-id="ceb45-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ceb45-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ceb45-111">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ceb45-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ceb45-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ceb45-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ceb45-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="ceb45-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="ceb45-114">[out] Um ponteiro para um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ceb45-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="ceb45-115">Se um aplicativo cliente transmite NULL no parâmetro _lppRestriction_ , **obter GetSearchCriteria** não retorna uma estrutura **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="ceb45-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="ceb45-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="ceb45-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="ceb45-117">[out] Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam os contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ceb45-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="ceb45-118">Se um cliente transmite NULL no parâmetro _lppContainerList_ , **obter GetSearchCriteria** não retorna uma matriz de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="ceb45-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="ceb45-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="ceb45-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="ceb45-120">[out] Um ponteiro para uma bitmask dos sinalizadores usados para indicar o estado atual da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ceb45-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="ceb45-121">Se um cliente transmite NULL no parâmetro _lpulSearchState_ , **obter GetSearchCriteria** não retorna nenhuma sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="ceb45-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="ceb45-122">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="ceb45-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="ceb45-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="ceb45-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="ceb45-124">A pesquisa deve ser executado em alta prioridade em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="ceb45-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="ceb45-125">Se esse sinalizador não estiver definida, a pesquisa é executado com prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="ceb45-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="ceb45-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="ceb45-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="ceb45-127">A pesquisa está no modo intensivo da CPU de sua operação, tentar localizar mensagens que correspondem aos critérios.</span><span class="sxs-lookup"><span data-stu-id="ceb45-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="ceb45-128">Se esse sinalizador não estiver definida, a parte de intensivo da CPU da operação de pesquisa é sobre.</span><span class="sxs-lookup"><span data-stu-id="ceb45-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="ceb45-129">Esse sinalizador tem significado apenas se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING está definido).</span><span class="sxs-lookup"><span data-stu-id="ceb45-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="ceb45-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="ceb45-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="ceb45-131">A pesquisa está procurando nos contêineres especificados e todos os seus contêineres filho para entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="ceb45-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="ceb45-132">Se esse sinalizador não estiver definida, somente os contêineres explicitamente incluídos na última chamada para o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) estão sendo pesquisados.</span><span class="sxs-lookup"><span data-stu-id="ceb45-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="ceb45-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="ceb45-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="ceb45-134">A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no repositório de mensagem ou o catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="ceb45-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="ceb45-135">Se esse sinalizador não estiver definida, a pesquisa está inativa e a tabela de conteúdo é estática.</span><span class="sxs-lookup"><span data-stu-id="ceb45-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ceb45-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ceb45-136">Return value</span></span>

<span data-ttu-id="ceb45-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="ceb45-137">S_OK</span></span> 
  
> <span data-ttu-id="ceb45-138">Os critérios de pesquisa foi obtida com êxito.</span><span class="sxs-lookup"><span data-stu-id="ceb45-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="ceb45-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ceb45-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ceb45-140">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="ceb45-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="ceb45-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ceb45-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="ceb45-142">Critérios de pesquisa nunca estabelecidos para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="ceb45-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ceb45-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceb45-143">Remarks</span></span>

<span data-ttu-id="ceb45-144">O método **IMAPIContainer::GetSearchCriteria** obtém os critérios de pesquisa para um contêiner que suporta pesquisas, geralmente, uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ceb45-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="ceb45-145">Você pode criar critérios de pesquisa chamando o método de **IMAPIContainer::SetSearchCriteria** de um contêiner.</span><span class="sxs-lookup"><span data-stu-id="ceb45-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ceb45-146">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="ceb45-146">Notes to implementers</span></span>

<span data-ttu-id="ceb45-147">Contêineres de catálogo de endereços, talvez seja necessário dar suporte ao **obter GetSearchCriteria** somente se eles oferecem as capacidades de pesquisa avançada associadas com a propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ceb45-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="ceb45-148">Para obter mais informações sobre como implementar o recurso de pesquisa avançada para contêineres do catálogo de endereços, consulte [Implementando a pesquisa avançada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="ceb45-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ceb45-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ceb45-149">Notes to callers</span></span>

<span data-ttu-id="ceb45-150">Quando tiver terminado com as estruturas de dados apontadas pelos parâmetros _lppRestriction_ e _lppContainerList_ , chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura ser liberada.</span><span class="sxs-lookup"><span data-stu-id="ceb45-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ceb45-151">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ceb45-151">MFCMAPI reference</span></span>

<span data-ttu-id="ceb45-152">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ceb45-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ceb45-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ceb45-153">**File**</span></span>|<span data-ttu-id="ceb45-154">**Function**</span><span class="sxs-lookup"><span data-stu-id="ceb45-154">**Function**</span></span>|<span data-ttu-id="ceb45-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ceb45-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ceb45-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ceb45-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ceb45-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ceb45-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="ceb45-158">MFCMAPI usa o método **IMAPIContainer::GetSearchCriteria** para obter os critérios de pesquisa de uma pasta para exibir.</span><span class="sxs-lookup"><span data-stu-id="ceb45-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ceb45-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceb45-159">See also</span></span>



[<span data-ttu-id="ceb45-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="ceb45-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="ceb45-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ceb45-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="ceb45-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ceb45-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ceb45-163">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="ceb45-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="ceb45-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ceb45-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="ceb45-165">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ceb45-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


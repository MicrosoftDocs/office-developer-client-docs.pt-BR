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
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412020"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="7f71e-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7f71e-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="7f71e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f71e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f71e-105">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f71e-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="7f71e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f71e-106">Parameters</span></span>

 <span data-ttu-id="7f71e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f71e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7f71e-108">[in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas.</span><span class="sxs-lookup"><span data-stu-id="7f71e-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="7f71e-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7f71e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7f71e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f71e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7f71e-111">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7f71e-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7f71e-112">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7f71e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7f71e-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="7f71e-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="7f71e-114">[out] Um ponteiro para um ponteiro para uma [estrutura SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f71e-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="7f71e-115">Se um aplicativo cliente passar NULL no parâmetro _lppRestriction,_ **GetSearchCriteria** não retornará uma **estrutura SRestriction.**</span><span class="sxs-lookup"><span data-stu-id="7f71e-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="7f71e-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="7f71e-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="7f71e-117">[out] Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f71e-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="7f71e-118">Se um cliente passar NULL no parâmetro  _lppContainerList,_ **GetSearchCriteria** não retornará uma matriz de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="7f71e-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="7f71e-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="7f71e-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="7f71e-120">[out] Um ponteiro para uma máscara de bits de sinalizadores usado para indicar o estado atual da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f71e-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="7f71e-121">Se um cliente passar NULL no parâmetro  _lpulSearchState,_ **GetSearchCriteria não** retornará sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="7f71e-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="7f71e-122">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7f71e-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="7f71e-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="7f71e-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="7f71e-124">A pesquisa deve ser executado com alta prioridade em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="7f71e-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="7f71e-125">Se esse sinalizador não estiver definido, a pesquisa será executado com prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="7f71e-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="7f71e-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="7f71e-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="7f71e-127">A pesquisa está no modo de uso intenso da CPU de sua operação, tentando localizar mensagens que corresponderem aos critérios.</span><span class="sxs-lookup"><span data-stu-id="7f71e-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="7f71e-128">Se esse sinalizador não estiver definido, a parte de uso intensivo da CPU da operação da pesquisa terminou.</span><span class="sxs-lookup"><span data-stu-id="7f71e-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="7f71e-129">Esse sinalizador só terá significado se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING estiver definido).</span><span class="sxs-lookup"><span data-stu-id="7f71e-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="7f71e-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="7f71e-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="7f71e-131">A pesquisa está procurando por entradas correspondentes em contêineres especificados e em todos os contêineres filho.</span><span class="sxs-lookup"><span data-stu-id="7f71e-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="7f71e-132">Se esse sinalizador não estiver definido, somente os contêineres incluídos explicitamente na última chamada para o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) serão pesquisados.</span><span class="sxs-lookup"><span data-stu-id="7f71e-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="7f71e-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="7f71e-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="7f71e-134">A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no armazenamento de mensagens ou no livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="7f71e-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="7f71e-135">Se esse sinalizador não estiver definido, a pesquisa será inativa e o índice de conteúdo será estático.</span><span class="sxs-lookup"><span data-stu-id="7f71e-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f71e-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7f71e-136">Return value</span></span>

<span data-ttu-id="7f71e-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f71e-137">S_OK</span></span> 
  
> <span data-ttu-id="7f71e-138">Os critérios de pesquisa foram obtidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="7f71e-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="7f71e-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7f71e-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7f71e-140">O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.</span><span class="sxs-lookup"><span data-stu-id="7f71e-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7f71e-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7f71e-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="7f71e-142">Os critérios de pesquisa nunca foram estabelecidos para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f71e-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f71e-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f71e-143">Remarks</span></span>

<span data-ttu-id="7f71e-144">O **método IMAPIContainer::GetSearchCriteria** obtém os critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7f71e-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="7f71e-145">Você cria critérios de pesquisa chamando o método **IMAPIContainer::SetSearchCriteria de** um contêiner.</span><span class="sxs-lookup"><span data-stu-id="7f71e-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7f71e-146">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7f71e-146">Notes to implementers</span></span>

<span data-ttu-id="7f71e-147">Os contêineres do livro de endereços talvez precisem dar suporte a **GetSearchCriteria** somente se eles fornecerem os recursos avançados de pesquisa associados à propriedade **PR_SEARCH** ([PidTagSearch).](pidtagsearch-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7f71e-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="7f71e-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="7f71e-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f71e-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7f71e-149">Notes to callers</span></span>

<span data-ttu-id="7f71e-150">Quando terminar as estruturas de dados apontadas pelos parâmetros  _lppRestriction_ e  _lppContainerList,_ chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="7f71e-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7f71e-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7f71e-151">MFCMAPI reference</span></span>

<span data-ttu-id="7f71e-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f71e-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7f71e-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7f71e-153">**File**</span></span>|<span data-ttu-id="7f71e-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="7f71e-154">**Function**</span></span>|<span data-ttu-id="7f71e-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7f71e-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f71e-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="7f71e-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="7f71e-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7f71e-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="7f71e-158">MFCMAPI usa o **método IMAPIContainer::GetSearchCriteria** para obter critérios de pesquisa de uma pasta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7f71e-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f71e-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f71e-159">See also</span></span>



[<span data-ttu-id="7f71e-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7f71e-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="7f71e-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7f71e-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="7f71e-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7f71e-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7f71e-163">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="7f71e-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="7f71e-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7f71e-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="7f71e-165">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7f71e-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


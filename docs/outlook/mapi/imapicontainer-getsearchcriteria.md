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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349291"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="7fc8b-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7fc8b-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="7fc8b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fc8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fc8b-105">Obtém os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="7fc8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fc8b-106">Parameters</span></span>

 <span data-ttu-id="7fc8b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7fc8b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7fc8b-108">no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="7fc8b-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7fc8b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7fc8b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7fc8b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7fc8b-111">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="7fc8b-112">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7fc8b-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="7fc8b-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="7fc8b-114">bota Um ponteiro para um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="7fc8b-115">Se um aplicativo cliente passar nulo no parâmetro _lppRestriction_ , **GetSearchCriteria** não retornará uma estrutura **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="7fc8b-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="7fc8b-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="7fc8b-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="7fc8b-117">bota Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="7fc8b-118">Se um cliente passar nulo no parâmetro _lppContainerList_ , **GetSearchCriteria** não retornará uma matriz de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="7fc8b-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="7fc8b-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="7fc8b-120">bota Um ponteiro para uma bitmask de sinalizadores usados para indicar o estado atual da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="7fc8b-121">Se um cliente passar nulo no parâmetro _lpulSearchState_ , **GetSearchCriteria** não retornará nenhum sinalizador.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="7fc8b-122">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7fc8b-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="7fc8b-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="7fc8b-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="7fc8b-124">A pesquisa deve ser executada com prioridade alta em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="7fc8b-125">Se esse sinalizador não for definido, a pesquisa será executada em prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="7fc8b-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="7fc8b-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="7fc8b-127">A pesquisa está no modo de CPU intensa de sua operação, tentando localizar mensagens que correspondam aos critérios.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="7fc8b-128">Se esse sinalizador não for definido, a parte intensiva da CPU da operação da pesquisa será sobre.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="7fc8b-129">Esse sinalizador tem significado somente se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING estiver definido).</span><span class="sxs-lookup"><span data-stu-id="7fc8b-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="7fc8b-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="7fc8b-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="7fc8b-131">A pesquisa está procurando por contêineres especificados e todos os seus contêineres filhos para entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="7fc8b-132">Se esse sinalizador não estiver definido, somente os contêineres incluídos explicitamente na última chamada para o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) estão sendo pesquisados.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="7fc8b-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="7fc8b-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="7fc8b-134">A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no repositório de mensagens ou no catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="7fc8b-135">Se esse sinalizador não for definido, a pesquisa estará inativa e a tabela de conteúdo será estática.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7fc8b-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7fc8b-136">Return value</span></span>

<span data-ttu-id="7fc8b-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fc8b-137">S_OK</span></span> 
  
> <span data-ttu-id="7fc8b-138">Os critérios de pesquisa foram obtidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="7fc8b-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7fc8b-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7fc8b-140">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="7fc8b-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7fc8b-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="7fc8b-142">Os critérios de pesquisa nunca foram estabelecidos para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fc8b-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fc8b-143">Remarks</span></span>

<span data-ttu-id="7fc8b-144">O método **IMAPIContainer:: GetSearchCriteria** Obtém os critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="7fc8b-145">Você cria critérios de pesquisa chamando o método **IMAPIContainer:: SetSearchCriteria** do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7fc8b-146">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="7fc8b-146">Notes to implementers</span></span>

<span data-ttu-id="7fc8b-147">Os contêineres do catálogo de endereços podem precisar de suporte para o **GetSearchCriteria** somente se eles fornecerem os recursos de pesquisa avançada associados à propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7fc8b-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="7fc8b-148">Para obter mais informações sobre como implementar o recurso de pesquisa avançada para contêineres do catálogo de endereços, consulte [implementação de pesquisa avançada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="7fc8b-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7fc8b-149">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7fc8b-149">Notes to callers</span></span>

<span data-ttu-id="7fc8b-150">Quando você tiver concluído as estruturas de dados apontadas pelos parâmetros _lppRestriction_ e _LppContainerList_ , chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura a ser liberada.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7fc8b-151">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7fc8b-151">MFCMAPI reference</span></span>

<span data-ttu-id="7fc8b-152">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7fc8b-153">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="7fc8b-153">**File**</span></span>|<span data-ttu-id="7fc8b-154">**Função**</span><span class="sxs-lookup"><span data-stu-id="7fc8b-154">**Function**</span></span>|<span data-ttu-id="7fc8b-155">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="7fc8b-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7fc8b-156">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="7fc8b-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="7fc8b-157">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7fc8b-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="7fc8b-158">MFCMAPI usa o método **IMAPIContainer:: GetSearchCriteria** para obter critérios de pesquisa de uma pasta a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="7fc8b-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fc8b-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fc8b-159">See also</span></span>



[<span data-ttu-id="7fc8b-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="7fc8b-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="7fc8b-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="7fc8b-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="7fc8b-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7fc8b-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7fc8b-163">Propriedade canônica PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="7fc8b-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="7fc8b-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7fc8b-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="7fc8b-165">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="7fc8b-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


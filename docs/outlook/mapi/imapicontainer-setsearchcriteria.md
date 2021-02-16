---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427196"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="82c42-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="82c42-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="82c42-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82c42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82c42-105">Estabelece critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c42-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="82c42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82c42-106">Parameters</span></span>

 <span data-ttu-id="82c42-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="82c42-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="82c42-108">[in] Um ponteiro para uma [estrutura SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="82c42-109">Se NULL for passado no  _parâmetro lpRestriction,_ os critérios de pesquisa usados mais recentemente para esse contêiner serão usados novamente.</span><span class="sxs-lookup"><span data-stu-id="82c42-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="82c42-110">NULL não deve ser passado  _em lpRestriction_ para a primeira pesquisa em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c42-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="82c42-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="82c42-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="82c42-112">[in] Um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="82c42-113">Se um cliente passar NULL no parâmetro  _lpContainerList,_ os identificadores de entrada usados mais recentemente para pesquisar esse contêiner serão usados para a nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="82c42-114">Um cliente não deve passar NULL em  _lpContainerList_ para a primeira pesquisa em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="82c42-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="82c42-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="82c42-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="82c42-116">[in] Uma máscara de bits de sinalizadores que controlam como a pesquisa é realizada.</span><span class="sxs-lookup"><span data-stu-id="82c42-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="82c42-117">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="82c42-117">The following flags can be set:</span></span>
    
<span data-ttu-id="82c42-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-119">A pesquisa deve ser executado com prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="82c42-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="82c42-120">Esse sinalizador não pode ser definido ao mesmo tempo que o FOREGROUND_SEARCH sinalizador.</span><span class="sxs-lookup"><span data-stu-id="82c42-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="82c42-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-122">A pesquisa deve ser executado com alta prioridade em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="82c42-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="82c42-123">Esse sinalizador não pode ser definido ao mesmo tempo que o BACKGROUND_SEARCH sinalizador.</span><span class="sxs-lookup"><span data-stu-id="82c42-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="82c42-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="82c42-125">A pesquisa não deve usar a indexação de conteúdo para encontrar entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="82c42-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="82c42-126">Esse sinalizador só é válido para armazenamentos do Exchange.</span><span class="sxs-lookup"><span data-stu-id="82c42-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="82c42-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-128">A pesquisa deve incluir os contêineres especificados no parâmetro  _lpContainerList_ e todos os contêineres filho.</span><span class="sxs-lookup"><span data-stu-id="82c42-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="82c42-129">Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador SHALLOW_SEARCH linha.</span><span class="sxs-lookup"><span data-stu-id="82c42-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="82c42-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-131">A pesquisa deve ser iniciada se esta for a primeira chamada para **SetSearchCriteria** ou reiniciada se a pesquisa estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="82c42-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="82c42-132">Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador STOP_SEARCH linha.</span><span class="sxs-lookup"><span data-stu-id="82c42-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="82c42-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-134">A pesquisa deve procurar apenas nos contêineres especificados no parâmetro  _lpContainerList_ para entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="82c42-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="82c42-135">Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador RECURSIVE_SEARCH linha.</span><span class="sxs-lookup"><span data-stu-id="82c42-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="82c42-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="82c42-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="82c42-137">A pesquisa deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="82c42-137">The search should be stopped.</span></span> <span data-ttu-id="82c42-138">Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador RESTART_SEARCH linha.</span><span class="sxs-lookup"><span data-stu-id="82c42-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82c42-139">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="82c42-139">Return value</span></span>

<span data-ttu-id="82c42-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="82c42-140">S_OK</span></span> 
  
> <span data-ttu-id="82c42-141">Os critérios de pesquisa foram definidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="82c42-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="82c42-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="82c42-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="82c42-143">O provedor de serviços não suporta os critérios de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="82c42-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82c42-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="82c42-144">Remarks</span></span>

<span data-ttu-id="82c42-145">O **método IMAPIContainer::SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="82c42-146">Uma pasta de resultados de pesquisa contém links para as mensagens que atendem aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais.</span><span class="sxs-lookup"><span data-stu-id="82c42-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="82c42-147">Os únicos dados exclusivos contidos em uma pasta de resultados de pesquisa são sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="82c42-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="82c42-148">O índice de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado do armazenamento de mensagens após a restrição de pesquisa ter sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="82c42-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="82c42-149">Uma operação de pesquisa funciona somente nesta tabela de conteúdo mesclado; ele não pesquisa por outras pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="82c42-150">Os resultados da pesquisa retornam apenas as mensagens que corresponderem aos critérios de pesquisa; a hierarquia de pastas não é retornada.</span><span class="sxs-lookup"><span data-stu-id="82c42-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="82c42-151">O controle é retornado ao cliente quando a pesquisa tiver sido concluída.</span><span class="sxs-lookup"><span data-stu-id="82c42-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="82c42-152">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="82c42-152">Notes to implementers</span></span>

<span data-ttu-id="82c42-153">Os contêineres de agendas estabelecem critérios de pesquisa aplicando restrições a seus índices de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="82c42-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="82c42-154">Para obter mais informações sobre critérios de pesquisa e contêineres de livro de endereços, consulte [Implementando Pesquisa Avançada.](implementing-advanced-searching.md)</span><span class="sxs-lookup"><span data-stu-id="82c42-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="82c42-155">Você deve dar suporte a operações de abrir, copiar, mover e excluir mensagens nas mensagens dentro de pastas de resultados de pesquisa, não na própria pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="82c42-156">Não permita que mensagens sejam criadas dentro ou copiadas em uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="82c42-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82c42-157">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="82c42-157">Notes to callers</span></span>

<span data-ttu-id="82c42-158">Para procurar destinatários de mensagem, de definida  _lpRestriction_ para apontar para uma restrição de subobjeto com o membro **ulSubObject** na [estrutura SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="82c42-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="82c42-159">Para procurar anexos, de definir o **membro ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="82c42-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="82c42-160">Definir o **membro lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos.</span><span class="sxs-lookup"><span data-stu-id="82c42-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="82c42-161">Por exemplo, para procurar anexos de arquivo que tenham a extensão .mss, de definir **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** e **lpRes** como uma restrição de propriedade que corresponde a **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) com .mss.</span><span class="sxs-lookup"><span data-stu-id="82c42-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="82c42-162">Definir o FOREGROUND_SEARCH sinalizador no  _parâmetro ulSearchFlags_ pode causar uma diminuição no desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="82c42-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="82c42-163">Você pode usar **SetSearchCriteria para** alterar os critérios de pesquisa de uma pesquisa já em andamento.</span><span class="sxs-lookup"><span data-stu-id="82c42-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="82c42-164">Você pode especificar novas restrições, novas listas de pastas a pesquisar e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="82c42-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="82c42-165">As alterações na prioridade da pesquisa não fazem com que uma pesquisa existente seja reiniciada, mas outras alterações nos critérios de pesquisa podem.</span><span class="sxs-lookup"><span data-stu-id="82c42-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="82c42-166">Quando você estiver usando uma pasta de resultados de pesquisa, poderá excluí-la ou deixá-la aberta para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="82c42-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="82c42-167">Se você excluir a pasta de resultados de pesquisa, somente os links de mensagens serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="82c42-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="82c42-168">As mensagens reais permanecem em suas pastas pai.</span><span class="sxs-lookup"><span data-stu-id="82c42-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="82c42-169">Para obter mais informações sobre pastas de resultados de pesquisa, consulte [MapI Search Folders](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="82c42-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="82c42-170">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="82c42-170">MFCMAPI reference</span></span>

<span data-ttu-id="82c42-171">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="82c42-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="82c42-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="82c42-172">**File**</span></span>|<span data-ttu-id="82c42-173">**Função**</span><span class="sxs-lookup"><span data-stu-id="82c42-173">**Function**</span></span>|<span data-ttu-id="82c42-174">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="82c42-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="82c42-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="82c42-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="82c42-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="82c42-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="82c42-177">MFCMAPI usa o **método IMAPIContainer::SetSearchCriteria** para gravar critérios de pesquisa para uma pasta após um usuário editá-la.</span><span class="sxs-lookup"><span data-stu-id="82c42-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82c42-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="82c42-178">See also</span></span>



[<span data-ttu-id="82c42-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="82c42-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="82c42-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="82c42-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="82c42-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="82c42-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="82c42-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="82c42-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="82c42-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="82c42-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="82c42-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="82c42-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="82c42-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="82c42-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="82c42-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82c42-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="82c42-187">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="82c42-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


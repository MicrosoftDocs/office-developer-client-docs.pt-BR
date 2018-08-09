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
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766954"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="46ce5-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="46ce5-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="46ce5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46ce5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46ce5-105">Estabelece os critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce5-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="46ce5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ce5-106">Parameters</span></span>

 <span data-ttu-id="46ce5-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="46ce5-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="46ce5-108">[in] Um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="46ce5-109">Se NULL é passada no parâmetro _lpRestriction_ , os critérios de pesquisa que foram usados mais recentemente para este contêiner são usados novamente.</span><span class="sxs-lookup"><span data-stu-id="46ce5-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="46ce5-110">NULL não deve ser passado no _lpRestriction_ para a pesquisa primeira em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce5-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="46ce5-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="46ce5-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="46ce5-112">[in] Um ponteiro para uma matriz de identificadores de entrada que representam os contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="46ce5-113">Se um cliente transmite NULL no parâmetro _lpContainerList_ , os identificadores de entrada usados mais recentemente para este contêiner de pesquisa são usados para a nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="46ce5-114">Um cliente não deve passar NULL no _lpContainerList_ para a pesquisa primeira em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="46ce5-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="46ce5-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="46ce5-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="46ce5-116">[in] Uma bitmask dos sinalizadores que controlam como a pesquisa é realizada.</span><span class="sxs-lookup"><span data-stu-id="46ce5-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="46ce5-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="46ce5-117">The following flags can be set:</span></span>
    
<span data-ttu-id="46ce5-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-119">A pesquisa deve ser executado com prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="46ce5-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="46ce5-120">Esse sinalizador não pode ser definida simultaneamente como o sinalizador FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="46ce5-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-122">A pesquisa deve ser executado em alta prioridade em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="46ce5-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="46ce5-123">Esse sinalizador não pode ser definida simultaneamente como o sinalizador BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="46ce5-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="46ce5-125">A pesquisa não deve usar a indexação de conteúdo para encontrar as entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="46ce5-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="46ce5-126">Esse sinalizador só é válida para repositórios do Exchange.</span><span class="sxs-lookup"><span data-stu-id="46ce5-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="46ce5-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-128">A pesquisa deve incluir os contêineres especificados no parâmetro _lpContainerList_ e todos os seus contêineres filho.</span><span class="sxs-lookup"><span data-stu-id="46ce5-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="46ce5-129">Esse sinalizador não pode ser definida simultaneamente como o sinalizador SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="46ce5-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-131">A pesquisa deve ser iniciada se esta for a primeira chamada para **definir SetSearchCriteria**ou reiniciada se a pesquisa está inativa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="46ce5-132">Esse sinalizador não pode ser definida simultaneamente como o sinalizador STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="46ce5-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-134">A pesquisa deve parecer apenas nos contêineres especificados no parâmetro _lpContainerList_ para entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="46ce5-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="46ce5-135">Esse sinalizador não pode ser definida simultaneamente como o sinalizador RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="46ce5-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="46ce5-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="46ce5-137">A pesquisa deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="46ce5-137">The search should be stopped.</span></span> <span data-ttu-id="46ce5-138">Esse sinalizador não pode ser definida simultaneamente como o sinalizador RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="46ce5-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46ce5-139">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="46ce5-139">Return value</span></span>

<span data-ttu-id="46ce5-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="46ce5-140">S_OK</span></span> 
  
> <span data-ttu-id="46ce5-141">Os critérios de pesquisa foi definida com êxito.</span><span class="sxs-lookup"><span data-stu-id="46ce5-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="46ce5-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="46ce5-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="46ce5-143">O provedor de serviços não suporta os critérios de pesquisa especificado.</span><span class="sxs-lookup"><span data-stu-id="46ce5-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46ce5-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ce5-144">Remarks</span></span>

<span data-ttu-id="46ce5-145">O método **IMAPIContainer::SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que suporta pesquisas, geralmente, uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="46ce5-146">Uma pasta de resultados de pesquisa contém links para as mensagens que atendam aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais.</span><span class="sxs-lookup"><span data-stu-id="46ce5-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="46ce5-147">Os dados somente exclusivos que estão contidos em uma pasta de resultados de pesquisa são sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="46ce5-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="46ce5-148">A tabela de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado o armazenamento de mensagens depois que tiver sido aplicada a restrição de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="46ce5-149">Uma operação de pesquisa funciona somente nesta tabela mescladas conteúdo; ele não procura por meio de outras pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="46ce5-150">Os resultados da pesquisa retornam somente as mensagens que correspondem aos critérios de pesquisa; a hierarquia de pastas não será retornada.</span><span class="sxs-lookup"><span data-stu-id="46ce5-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="46ce5-151">Controle é retornado ao cliente quando a conclusão da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="46ce5-152">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="46ce5-152">Notes to implementers</span></span>

<span data-ttu-id="46ce5-153">Contêineres de catálogo de endereços estabelecer critérios de pesquisa aplicando restrições ao suas tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="46ce5-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="46ce5-154">Para obter mais informações sobre os critérios de pesquisa e contêineres do catálogo de endereços, consulte [Implementando a pesquisa avançada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="46ce5-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="46ce5-155">Você deve suportar open, copiar, mover e excluir operações em todas as mensagens em pastas de resultados da pesquisa, não na pasta de resultados de pesquisa em si.</span><span class="sxs-lookup"><span data-stu-id="46ce5-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="46ce5-156">Não permitir que as mensagens sejam criados dentro ou copiados para uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="46ce5-157">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="46ce5-157">Notes to callers</span></span>

<span data-ttu-id="46ce5-158">Para pesquisar os destinatários da mensagem, defina _lpRestriction_ para apontar para uma restrição subobjeto com o membro **ulSubObject** na estrutura de [SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="46ce5-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="46ce5-159">Para procurar anexos, defina o membro **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="46ce5-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="46ce5-160">Defina o membro **lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos.</span><span class="sxs-lookup"><span data-stu-id="46ce5-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="46ce5-161">Por exemplo, para procurar anexos de arquivo com a extensão .mss, defina **ulSubObject** **PR_MESSAGE_ATTACHMENTS** e **lpRes** para uma restrição de propriedade que corresponda **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) com. mss.</span><span class="sxs-lookup"><span data-stu-id="46ce5-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="46ce5-162">Definir o sinalizador FOREGROUND_SEARCH no parâmetro _ulSearchFlags_ pode causar uma diminuição no desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="46ce5-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="46ce5-163">Você pode usar **definir SetSearchCriteria** para alterar os critérios de pesquisa de uma pesquisa já está em andamento.</span><span class="sxs-lookup"><span data-stu-id="46ce5-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="46ce5-164">Você pode especificar novas restrições, novas listas de pastas a serem pesquisadas e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="46ce5-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="46ce5-165">Alterações na ordem de prioridade de pesquisa não farão com que uma pesquisa existente reiniciar, mas podem outras alterações aos critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="46ce5-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="46ce5-166">Quando você estiver por meio do uso de uma pasta de resultados de pesquisa, você pode excluir a pasta ou deixá-lo a permanecer abertas para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="46ce5-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="46ce5-167">Se você excluir a pasta de resultados de pesquisa, somente os links de mensagem serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="46ce5-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="46ce5-168">As mensagens reais permanecem em suas pastas pai.</span><span class="sxs-lookup"><span data-stu-id="46ce5-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="46ce5-169">Para obter mais informações sobre as pastas de resultados da pesquisa, consulte [Pastas de pesquisa de MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="46ce5-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="46ce5-170">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="46ce5-170">MFCMAPI reference</span></span>

<span data-ttu-id="46ce5-171">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="46ce5-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="46ce5-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="46ce5-172">**File**</span></span>|<span data-ttu-id="46ce5-173">**Function**</span><span class="sxs-lookup"><span data-stu-id="46ce5-173">**Function**</span></span>|<span data-ttu-id="46ce5-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="46ce5-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46ce5-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="46ce5-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="46ce5-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="46ce5-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="46ce5-177">MFCMAPI usa o método **IMAPIContainer::SetSearchCriteria** para gravar os critérios de pesquisa para uma pasta depois que um usuário tenha editado-lo.</span><span class="sxs-lookup"><span data-stu-id="46ce5-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46ce5-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="46ce5-178">See also</span></span>



[<span data-ttu-id="46ce5-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="46ce5-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="46ce5-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="46ce5-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="46ce5-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="46ce5-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="46ce5-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="46ce5-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="46ce5-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="46ce5-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="46ce5-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="46ce5-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="46ce5-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="46ce5-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="46ce5-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="46ce5-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="46ce5-187">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="46ce5-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350964"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="40ce8-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="40ce8-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="40ce8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40ce8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40ce8-105">Estabelece critérios de pesquisa para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="40ce8-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="40ce8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40ce8-106">Parameters</span></span>

 <span data-ttu-id="40ce8-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="40ce8-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="40ce8-108">no Um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="40ce8-109">Se NULL for passado no parâmetro _lpRestriction_ , os critérios de pesquisa que foram usados mais recentemente para este contêiner serão usados novamente.</span><span class="sxs-lookup"><span data-stu-id="40ce8-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="40ce8-110">NULL não deve ser passado no _lpRestriction_ para a primeira pesquisa em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="40ce8-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="40ce8-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="40ce8-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="40ce8-112">no Um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="40ce8-113">Se um cliente passa nulo no parâmetro _lpContainerList_ , os identificadores de entrada usados mais recentemente para pesquisar esse contêiner são usados para a nova pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="40ce8-114">Um cliente não deve passar nulo no _lpContainerList_ para a primeira pesquisa em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="40ce8-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="40ce8-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="40ce8-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="40ce8-116">no Uma bitmask de sinalizadores que controlam como a pesquisa é realizada.</span><span class="sxs-lookup"><span data-stu-id="40ce8-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="40ce8-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="40ce8-117">The following flags can be set:</span></span>
    
<span data-ttu-id="40ce8-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-119">A pesquisa deve ser executada em prioridade normal em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="40ce8-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="40ce8-120">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador FOREGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="40ce8-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-122">A pesquisa deve ser executada com prioridade alta em relação a outras pesquisas.</span><span class="sxs-lookup"><span data-stu-id="40ce8-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="40ce8-123">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador BACKGROUND_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="40ce8-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="40ce8-125">A pesquisa não deve usar a indexação de conteúdo para localizar entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="40ce8-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="40ce8-126">Este sinalizador só é válido para repositórios do Exchange.</span><span class="sxs-lookup"><span data-stu-id="40ce8-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="40ce8-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-128">A pesquisa deve incluir os contêineres especificados no parâmetro _lpContainerList_ e todos os seus contêineres filhos.</span><span class="sxs-lookup"><span data-stu-id="40ce8-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="40ce8-129">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador SHALLOW_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="40ce8-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-131">A pesquisa deve ser iniciada se esta for a primeira chamada para **SetSearchCriteria**ou reiniciada se a pesquisa estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="40ce8-132">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador STOP_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="40ce8-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-134">A pesquisa deve procurar somente nos contêineres especificados no parâmetro _lpContainerList_ para entradas correspondentes.</span><span class="sxs-lookup"><span data-stu-id="40ce8-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="40ce8-135">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador RECURSIVE_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="40ce8-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="40ce8-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="40ce8-137">A pesquisa deve ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="40ce8-137">The search should be stopped.</span></span> <span data-ttu-id="40ce8-138">Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador RESTART_SEARCH.</span><span class="sxs-lookup"><span data-stu-id="40ce8-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="40ce8-139">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="40ce8-139">Return value</span></span>

<span data-ttu-id="40ce8-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="40ce8-140">S_OK</span></span> 
  
> <span data-ttu-id="40ce8-141">Os critérios de pesquisa foram definidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="40ce8-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="40ce8-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="40ce8-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="40ce8-143">O provedor de serviços não oferece suporte aos critérios de pesquisa especificados.</span><span class="sxs-lookup"><span data-stu-id="40ce8-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40ce8-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="40ce8-144">Remarks</span></span>

<span data-ttu-id="40ce8-145">O método **IMAPIContainer:: SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="40ce8-146">Uma pasta de resultados de pesquisa contém links para as mensagens que atendem aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais.</span><span class="sxs-lookup"><span data-stu-id="40ce8-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="40ce8-147">Os únicos dados exclusivos que estão contidos em uma pasta de resultados de pesquisa é sua tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="40ce8-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="40ce8-148">A tabela de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado do repositório de mensagens após a restrição de pesquisa ter sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="40ce8-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="40ce8-149">Uma operação de pesquisa funciona somente nesta tabela de conteúdo mesclado; Ele não pesquisa por outras pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="40ce8-150">Os resultados da pesquisa retornam apenas as mensagens que correspondem aos critérios de pesquisa; a hierarquia de pastas não é retornada.</span><span class="sxs-lookup"><span data-stu-id="40ce8-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="40ce8-151">O controle é retornado ao cliente quando a pesquisa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="40ce8-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="40ce8-152">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="40ce8-152">Notes to implementers</span></span>

<span data-ttu-id="40ce8-153">Os contêineres do catálogo de endereços estabelecem critérios de pesquisa aplicando restrições às tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="40ce8-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="40ce8-154">Para obter mais informações sobre critérios de pesquisa e contêineres do catálogo de endereços, consulte [implementaNdo pesquisa avançada](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="40ce8-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="40ce8-155">Você deve oferecer suporte a operações abrir, copiar, mover e excluir nas mensagens dentro das pastas de resultados de pesquisa, e não na própria pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="40ce8-156">Não permite que as mensagens sejam criadas dentro ou copiadas para uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="40ce8-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="40ce8-157">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="40ce8-157">Notes to callers</span></span>

<span data-ttu-id="40ce8-158">Para procurar destinatários de mensagens, defina _lpRestriction_ para apontar para uma restrição de subobjeto com o membro **UlSubObject** na estrutura [SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40ce8-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="40ce8-159">Para procurar anexos, defina o membro **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="40ce8-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="40ce8-160">Defina o membro **lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos.</span><span class="sxs-lookup"><span data-stu-id="40ce8-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="40ce8-161">Por exemplo, para procurar anexos de arquivo com a extensão. MSS, defina **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** e **lpRes** como uma restrição de propriedade que corresponda a **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) com. MSS.</span><span class="sxs-lookup"><span data-stu-id="40ce8-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="40ce8-162">Definir o sinalizador FOREGROUND_SEARCH no parâmetro _ulSearchFlags_ pode causar uma redução no desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="40ce8-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="40ce8-163">Você pode usar o **SetSearchCriteria** para alterar os critérios de pesquisa de uma pesquisa já em andamento.</span><span class="sxs-lookup"><span data-stu-id="40ce8-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="40ce8-164">Você pode especificar novas restrições, novas listas de pastas a serem pesquisadas e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="40ce8-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="40ce8-165">As alterações na prioridade de pesquisa não fazem com que uma pesquisa existente seja reiniciada, mas outras alterações nos critérios de pesquisa podem.</span><span class="sxs-lookup"><span data-stu-id="40ce8-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="40ce8-166">Quando você usa uma pasta de resultados de pesquisa, você pode excluir a pasta ou deixá-la permanecer aberta para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="40ce8-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="40ce8-167">Se você excluir a pasta de resultados de pesquisa, somente os links de mensagens serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="40ce8-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="40ce8-168">As mensagens reais permanecem em suas pastas pai.</span><span class="sxs-lookup"><span data-stu-id="40ce8-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="40ce8-169">Para obter mais informações sobre pastas de resultados de pesquisa, consulte [pastas de pesquisa MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="40ce8-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="40ce8-170">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="40ce8-170">MFCMAPI reference</span></span>

<span data-ttu-id="40ce8-171">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="40ce8-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="40ce8-172">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="40ce8-172">**File**</span></span>|<span data-ttu-id="40ce8-173">**Função**</span><span class="sxs-lookup"><span data-stu-id="40ce8-173">**Function**</span></span>|<span data-ttu-id="40ce8-174">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="40ce8-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="40ce8-175">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="40ce8-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="40ce8-176">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="40ce8-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="40ce8-177">MFCMAPI usa o método **IMAPIContainer:: SetSearchCriteria** para gravar critérios de pesquisa para uma pasta após o usuário ter editado.</span><span class="sxs-lookup"><span data-stu-id="40ce8-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40ce8-178">Confira também</span><span class="sxs-lookup"><span data-stu-id="40ce8-178">See also</span></span>



[<span data-ttu-id="40ce8-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="40ce8-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="40ce8-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="40ce8-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="40ce8-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="40ce8-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="40ce8-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="40ce8-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="40ce8-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="40ce8-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="40ce8-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="40ce8-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="40ce8-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="40ce8-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="40ce8-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="40ce8-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="40ce8-187">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="40ce8-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


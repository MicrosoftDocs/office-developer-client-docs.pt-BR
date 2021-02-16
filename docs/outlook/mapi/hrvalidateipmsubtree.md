---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436570"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="f8b95-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f8b95-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="f8b95-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8b95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8b95-105">Adiciona pastas de mensagens padrão interpersonal (IPM) a um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8b95-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8b95-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f8b95-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8b95-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f8b95-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f8b95-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f8b95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f8b95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f8b95-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f8b95-110">Called by:</span></span>  <br/> |<span data-ttu-id="f8b95-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="f8b95-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="f8b95-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8b95-112">Parameters</span></span>

 <span data-ttu-id="f8b95-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="f8b95-113">_lpMDB_</span></span>
  
> <span data-ttu-id="f8b95-114">[in] Ponteiro para o objeto de armazenamento de mensagens ao qual adicionar as pastas.</span><span class="sxs-lookup"><span data-stu-id="f8b95-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="f8b95-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8b95-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f8b95-116">[in] Bitmask de sinalizadores usados para controlar como as pastas são criadas.</span><span class="sxs-lookup"><span data-stu-id="f8b95-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="f8b95-117">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f8b95-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f8b95-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f8b95-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="f8b95-119">As pastas devem ser verificadas antes da criação, mesmo se as propriedades do armazenamento de mensagens indicarem que são válidas.</span><span class="sxs-lookup"><span data-stu-id="f8b95-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="f8b95-120">Um aplicativo cliente normalmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada.</span><span class="sxs-lookup"><span data-stu-id="f8b95-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="f8b95-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="f8b95-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="f8b95-122">O conjunto completo de pastas IPM deve ser criado na pasta raiz do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8b95-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="f8b95-123">Os títulos de pasta na hierarquia são:</span><span class="sxs-lookup"><span data-stu-id="f8b95-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="f8b95-124">Exibições de Pasta</span><span class="sxs-lookup"><span data-stu-id="f8b95-124">Folder Views</span></span>
    
    - <span data-ttu-id="f8b95-125">Exibições comuns</span><span class="sxs-lookup"><span data-stu-id="f8b95-125">Common Views</span></span>
    
    - <span data-ttu-id="f8b95-126">Raiz de Pesquisa\*</span><span class="sxs-lookup"><span data-stu-id="f8b95-126">Search Root\*</span></span>
    
    - <span data-ttu-id="f8b95-127">Subárvore IPM\*</span><span class="sxs-lookup"><span data-stu-id="f8b95-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="f8b95-128">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="f8b95-128">Inbox</span></span>
    
    - <span data-ttu-id="f8b95-129">Caixa de saída</span><span class="sxs-lookup"><span data-stu-id="f8b95-129">Outbox</span></span>
    
    - <span data-ttu-id="f8b95-130">Itens excluídos\*</span><span class="sxs-lookup"><span data-stu-id="f8b95-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="f8b95-131">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="f8b95-131">Sent Items</span></span>
    
    <span data-ttu-id="f8b95-132">onde as três pastas marcadas com são o conjunto mínimo criado mesmo quando o \* MAPI_FULL_IPM_TREE sinalizador não foi definido.</span><span class="sxs-lookup"><span data-stu-id="f8b95-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="f8b95-133">Um aplicativo cliente normalmente define esse sinalizador quando o armazenamento de mensagens no qual as pastas devem ser criadas é o armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="f8b95-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="f8b95-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="f8b95-134">_lpcValues_</span></span>
  
> <span data-ttu-id="f8b95-135">[in, out] Ponteiro para o número de [estruturas SPropValue](spropvalue.md) na matriz retornada no _parâmetro lppProps._</span><span class="sxs-lookup"><span data-stu-id="f8b95-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="f8b95-136">O valor do parâmetro  _lpcValues_ pode ser zero se  _lppProps_ for NULL.</span><span class="sxs-lookup"><span data-stu-id="f8b95-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="f8b95-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="f8b95-137">_lppProps_</span></span>
  
> <span data-ttu-id="f8b95-138">[in, out] Ponteiro para um ponteiro para uma matriz de **estruturas SPropValue** que contém valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e para as propriedades de identificador de entrada de pasta apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f8b95-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="f8b95-139">Se **HrValidateIPMSubtree** criar uma Caixa de Entrada no armazenamento de mensagens, a matriz **SPropValue** incluirá um identificador de entrada de Caixa de Entrada com uma marca de propriedade especial codificada como  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` .</span><span class="sxs-lookup"><span data-stu-id="f8b95-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="f8b95-140">O  _parâmetro lppProps_ pode ser NULL, indicando que a implementação da chamada não exige que uma **matriz SPropValue** seja retornada.</span><span class="sxs-lookup"><span data-stu-id="f8b95-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="f8b95-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f8b95-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="f8b95-142">[out] Ponteiro para um ponteiro para uma [estrutura MAPIERROR](mapierror.md) que contém informações de versão, componente e contexto para um erro.</span><span class="sxs-lookup"><span data-stu-id="f8b95-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="f8b95-143">O  _parâmetro lppMAPIError_ é definido como NULL se nenhuma **estrutura MAPIERROR** for retornada.</span><span class="sxs-lookup"><span data-stu-id="f8b95-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8b95-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8b95-144">Return value</span></span>

<span data-ttu-id="f8b95-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f8b95-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8b95-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8b95-146">Remarks</span></span>

<span data-ttu-id="f8b95-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span><span class="sxs-lookup"><span data-stu-id="f8b95-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="f8b95-148">Essa função também pode ser usada por aplicativos cliente para validar ou reparar pastas de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="f8b95-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="f8b95-149">**HrValidateIPMSubtree** sempre cria as pastas Raiz de Pesquisa e Subárvore do IPM na pasta raiz do armazenamento e a pasta Itens Excluídos na pasta Subárvore do IPM.</span><span class="sxs-lookup"><span data-stu-id="f8b95-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="f8b95-150">A pasta Subárvore do IPM é a raiz da hierarquia do IPM nesse armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8b95-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="f8b95-151">A pasta Raiz da Pesquisa pode ser usada como raiz de uma subárvore para pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f8b95-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="f8b95-152">Os clientes IPM devem exibir a exibição de pastas começando na pasta raiz da subárvore do IPM e mostrando pastas filho abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="f8b95-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="f8b95-153">As informações na pasta raiz de um armazenamento de mensagens não devem aparecer na interface do usuário de um cliente.</span><span class="sxs-lookup"><span data-stu-id="f8b95-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="f8b95-154">Essa funcionalidade significa que, se um cliente tiver que ocultar informações, as informações poderão ser colocadas no diretório raiz da subárvore do IPM, onde não estarão visíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="f8b95-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="f8b95-155">Por outro lado, aplicativos não IPM que exigem que mensagens e pastas sejam invisíveis para o usuário, por exemplo, em um armazenamento de mensagens baseado em servidor, podem colocá-los fora da hierarquia do IPM.</span><span class="sxs-lookup"><span data-stu-id="f8b95-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="f8b95-156">**HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM criada tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="f8b95-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="f8b95-157">As seguintes propriedades do identificador de entrada do armazenamento de mensagens são definidas para os identificadores de entrada das pastas correspondentes e retornadas no parâmetro  _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="f8b95-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="f8b95-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f8b95-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f8b95-165">Um espaço reservado [PROP_TAG](prop_tag.md) para a Caixa de Entrada do IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f8b95-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8b95-166">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f8b95-166">MFCMAPI reference</span></span>

<span data-ttu-id="f8b95-167">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8b95-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8b95-168">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="f8b95-168">**File**</span></span>|<span data-ttu-id="f8b95-169">**Função**</span><span class="sxs-lookup"><span data-stu-id="f8b95-169">**Function**</span></span>|<span data-ttu-id="f8b95-170">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="f8b95-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8b95-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f8b95-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f8b95-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f8b95-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="f8b95-173">MFCMAPI usa o **método HrValidateIPMSubtree** para adicionar pastas padrão a um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f8b95-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8b95-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8b95-174">See also</span></span>



[<span data-ttu-id="f8b95-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f8b95-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="f8b95-176">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="f8b95-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


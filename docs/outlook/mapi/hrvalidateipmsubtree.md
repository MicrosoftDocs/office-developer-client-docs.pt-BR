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
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592042"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="1529f-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="1529f-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="1529f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1529f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1529f-105">Adiciona as pastas de mensagem padrão interpessoais (IPM) para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1529f-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1529f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1529f-106">Header file:</span></span>  <br/> |<span data-ttu-id="1529f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1529f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1529f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="1529f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1529f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1529f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1529f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="1529f-110">Called by:</span></span>  <br/> |<span data-ttu-id="1529f-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="1529f-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="1529f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1529f-112">Parameters</span></span>

 <span data-ttu-id="1529f-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="1529f-113">_lpMDB_</span></span>
  
> <span data-ttu-id="1529f-114">[in] Ponteiro para a mensagem armazenar o objeto ao qual adicionar as pastas.</span><span class="sxs-lookup"><span data-stu-id="1529f-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="1529f-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1529f-115">_ulFlags_</span></span>
  
> <span data-ttu-id="1529f-116">[in] Bitmask dos sinalizadores usadas para controlar como as pastas são criadas.</span><span class="sxs-lookup"><span data-stu-id="1529f-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="1529f-117">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1529f-117">The following flags can be set:</span></span>
    
<span data-ttu-id="1529f-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="1529f-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="1529f-119">As pastas devem ser verificadas antes da criação, mesmo se o repositório de propriedades da mensagem indicam que eles são válidos.</span><span class="sxs-lookup"><span data-stu-id="1529f-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="1529f-120">Um aplicativo cliente geralmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada.</span><span class="sxs-lookup"><span data-stu-id="1529f-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="1529f-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="1529f-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="1529f-122">O conjunto completo de pastas IPM deve ser criado na pasta raiz do repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1529f-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="1529f-123">Os títulos de pasta na hierarquia são:</span><span class="sxs-lookup"><span data-stu-id="1529f-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="1529f-124">Modos de exibição de pasta</span><span class="sxs-lookup"><span data-stu-id="1529f-124">Folder Views</span></span>
    
    - <span data-ttu-id="1529f-125">Modos de exibição comuns</span><span class="sxs-lookup"><span data-stu-id="1529f-125">Common Views</span></span>
    
    - <span data-ttu-id="1529f-126">Raiz de pesquisa\*</span><span class="sxs-lookup"><span data-stu-id="1529f-126">Search Root\*</span></span>
    
    - <span data-ttu-id="1529f-127">Subárvore IPM\*</span><span class="sxs-lookup"><span data-stu-id="1529f-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="1529f-128">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="1529f-128">Inbox</span></span>
    
    - <span data-ttu-id="1529f-129">Caixa de saída</span><span class="sxs-lookup"><span data-stu-id="1529f-129">Outbox</span></span>
    
    - <span data-ttu-id="1529f-130">Itens excluídos\*</span><span class="sxs-lookup"><span data-stu-id="1529f-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="1529f-131">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="1529f-131">Sent Items</span></span>
    
    <span data-ttu-id="1529f-132">onde as três pastas marcadas com \* são o conjunto mínimo criado mesmo quando o sinalizador MAPI_FULL_IPM_TREE não foi definido.</span><span class="sxs-lookup"><span data-stu-id="1529f-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="1529f-133">Um aplicativo cliente geralmente define esse sinalizador quando o armazenamento de mensagens em que as pastas devem ser criados é o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="1529f-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="1529f-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="1529f-134">_lpcValues_</span></span>
  
> <span data-ttu-id="1529f-135">[além, out] Ponteiro para o número de estruturas de [SPropValue](spropvalue.md) na matriz retornada no parâmetro _lppProps_ .</span><span class="sxs-lookup"><span data-stu-id="1529f-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="1529f-136">O valor do parâmetro _lpcValues_ pode ser zero se _lppProps_ é NULL.</span><span class="sxs-lookup"><span data-stu-id="1529f-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="1529f-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="1529f-137">_lppProps_</span></span>
  
> <span data-ttu-id="1529f-138">[além, out] Ponteiro para um ponteiro para uma matriz de estruturas de **SPropValue** que contém os valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e as propriedades de identificador de entrada de pasta apropriada.</span><span class="sxs-lookup"><span data-stu-id="1529f-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="1529f-139">Se **HrValidateIPMSubtree** cria uma caixa de entrada no repositório de mensagem, a matriz de **SPropValue** inclui um identificador de entrada da caixa de entrada com uma marca de propriedade especial codificada como `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span><span class="sxs-lookup"><span data-stu-id="1529f-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="1529f-140">O parâmetro _lppProps_ pode ser NULL, indicando que a implementação de chamada não exige que uma matriz **SPropValue** ser retornado.</span><span class="sxs-lookup"><span data-stu-id="1529f-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="1529f-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="1529f-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="1529f-142">[out] Ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) que contém informações de versão, componente e contexto para um erro.</span><span class="sxs-lookup"><span data-stu-id="1529f-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="1529f-143">O parâmetro _lppMAPIError_ é definido como NULL se nenhuma estrutura **MAPIERROR** é retornada.</span><span class="sxs-lookup"><span data-stu-id="1529f-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1529f-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1529f-144">Return value</span></span>

<span data-ttu-id="1529f-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1529f-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1529f-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="1529f-146">Remarks</span></span>

<span data-ttu-id="1529f-147">MAPI usa a função **HrValidateIPMSubtree** internamente para construir a subárvore IPM padrão em um repositório de mensagem quando o armazenamento é aberto pela primeira vez ou quando um repositório é feito padrão armazenar.</span><span class="sxs-lookup"><span data-stu-id="1529f-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="1529f-148">Essa função também pode ser usada pelos aplicativos cliente para validar ou reparar as pastas de mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="1529f-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="1529f-149">**HrValidateIPMSubtree** sempre cria as pastas raiz de pesquisa e subárvore IPM na pasta raiz do repositório e a pasta Itens excluídos na pasta subárvore IPM.</span><span class="sxs-lookup"><span data-stu-id="1529f-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="1529f-150">A pasta subárvore IPM é a raiz da hierarquia IPM desse repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1529f-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="1529f-151">A pasta raiz de pesquisa pode ser usada como a raiz de uma subárvore para pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1529f-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="1529f-152">Clientes IPM devem exibição de suas pastas começando na pasta raiz de subárvore IPM e mostrando filho pastas sob ele.</span><span class="sxs-lookup"><span data-stu-id="1529f-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="1529f-153">Informações na pasta raiz de um repositório de mensagem não devem aparecer na interface do usuário do cliente.</span><span class="sxs-lookup"><span data-stu-id="1529f-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="1529f-154">Essa funcionalidade significa que se um cliente deve ocultar as informações, as informações podem ser colocadas no diretório raiz subárvore IPM, onde não é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="1529f-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="1529f-155">Por outro lado, os aplicativos de não-IPM que exigem mensagens e pastas invisível ao usuário, por exemplo, em um armazenamento de mensagens baseado em servidor, podem colocá-los fora da hierarquia IPM.</span><span class="sxs-lookup"><span data-stu-id="1529f-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="1529f-156">**HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM cria tem um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="1529f-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="1529f-157">As seguintes propriedades do identificador de entrada do repositório de mensagem estiver definidas como os identificadores de entrada das pastas correspondentes e retornadas no parâmetro _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="1529f-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="1529f-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1529f-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="1529f-165">Um espaço reservado [PROP_TAG](prop_tag.md) para a caixa de entrada IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="1529f-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="1529f-166">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1529f-166">MFCMAPI reference</span></span>

<span data-ttu-id="1529f-167">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1529f-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1529f-168">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1529f-168">**File**</span></span>|<span data-ttu-id="1529f-169">**Function**</span><span class="sxs-lookup"><span data-stu-id="1529f-169">**Function**</span></span>|<span data-ttu-id="1529f-170">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1529f-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1529f-171">MstStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="1529f-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="1529f-172">CMsgStoreDlg::OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="1529f-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="1529f-173">MFCMAPI usa o método **HrValidateIPMSubtree** para adicionar pastas padrão para um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1529f-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1529f-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="1529f-174">See also</span></span>



[<span data-ttu-id="1529f-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="1529f-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="1529f-176">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1529f-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


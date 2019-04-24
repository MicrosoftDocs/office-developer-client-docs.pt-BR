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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346764"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="69189-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="69189-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="69189-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69189-105">Adiciona pastas padrão de mensagens interpessoais (IPM) a um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="69189-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69189-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="69189-106">Header file:</span></span>  <br/> |<span data-ttu-id="69189-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="69189-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="69189-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="69189-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="69189-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="69189-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="69189-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="69189-110">Called by:</span></span>  <br/> |<span data-ttu-id="69189-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="69189-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="69189-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69189-112">Parameters</span></span>

 <span data-ttu-id="69189-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="69189-113">_lpMDB_</span></span>
  
> <span data-ttu-id="69189-114">no Ponteiro para o objeto do repositório de mensagens ao qual as pastas serão adicionadas.</span><span class="sxs-lookup"><span data-stu-id="69189-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="69189-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69189-115">_ulFlags_</span></span>
  
> <span data-ttu-id="69189-116">no Bitmask dos sinalizadores usados para controlar como as pastas são criadas.</span><span class="sxs-lookup"><span data-stu-id="69189-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="69189-117">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="69189-117">The following flags can be set:</span></span>
    
<span data-ttu-id="69189-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="69189-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="69189-119">As pastas devem ser verificadas antes da criação, mesmo se as propriedades do repositório de mensagens indicarem que são válidas.</span><span class="sxs-lookup"><span data-stu-id="69189-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="69189-120">Um aplicativo cliente normalmente define esse sinalizador quando um erro indica que a estrutura de uma pasta existente foi danificada.</span><span class="sxs-lookup"><span data-stu-id="69189-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="69189-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="69189-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="69189-122">O conjunto completo de pastas IPM deve ser criado na pasta raiz do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="69189-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="69189-123">Os títulos de pasta na hierarquia são:</span><span class="sxs-lookup"><span data-stu-id="69189-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="69189-124">Modos de exibição de pasta</span><span class="sxs-lookup"><span data-stu-id="69189-124">Folder Views</span></span>
    
    - <span data-ttu-id="69189-125">Modos de exibição comuns</span><span class="sxs-lookup"><span data-stu-id="69189-125">Common Views</span></span>
    
    - <span data-ttu-id="69189-126">Raiz de pesquisa\*</span><span class="sxs-lookup"><span data-stu-id="69189-126">Search Root\*</span></span>
    
    - <span data-ttu-id="69189-127">SubÁrvore IPM\*</span><span class="sxs-lookup"><span data-stu-id="69189-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="69189-128">Caixa de Entrada</span><span class="sxs-lookup"><span data-stu-id="69189-128">Inbox</span></span>
    
    - <span data-ttu-id="69189-129">Enviada</span><span class="sxs-lookup"><span data-stu-id="69189-129">Outbox</span></span>
    
    - <span data-ttu-id="69189-130">Itens excluídos\*</span><span class="sxs-lookup"><span data-stu-id="69189-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="69189-131">Itens enviados</span><span class="sxs-lookup"><span data-stu-id="69189-131">Sent Items</span></span>
    
    <span data-ttu-id="69189-132">onde as três pastas marcadas \* com são o conjunto mínimo criado, mesmo quando o sinalizador MAPI_FULL_IPM_TREE não foi definido.</span><span class="sxs-lookup"><span data-stu-id="69189-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="69189-133">Um aplicativo cliente normalmente define esse sinalizador quando o repositório de mensagens no qual as pastas devem ser criadas é o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="69189-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="69189-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="69189-134">_lpcValues_</span></span>
  
> <span data-ttu-id="69189-135">[in, out] Ponteiro para o número de estruturas [SPropValue](spropvalue.md) na matriz retornada no parâmetro _lppProps_ .</span><span class="sxs-lookup"><span data-stu-id="69189-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="69189-136">O valor do parâmetro _lpcValues_ pode ser zero se _lppProps_ for nulo.</span><span class="sxs-lookup"><span data-stu-id="69189-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="69189-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="69189-137">_lppProps_</span></span>
  
> <span data-ttu-id="69189-138">[in, out] Ponteiro para um ponteiro para uma matriz de estruturas **SPropValue** que contém valores de propriedade para a propriedade **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) e para as propriedades de identificador de entrada de pasta apropriadas.</span><span class="sxs-lookup"><span data-stu-id="69189-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="69189-139">Se **HrValidateIPMSubtree** cria uma caixa de entrada no repositório de mensagens, a matriz **SPropValue** inclui um identificador de entrada de caixa de entrada com uma `PROP_TAG(PT_BINARY, PROP_ID_NULL)`marca de propriedade especial codificada como.</span><span class="sxs-lookup"><span data-stu-id="69189-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="69189-140">O parâmetro _lppProps_ pode ser NULL, indicando que a implementação de chamada não exige que uma matriz **SPropValue** seja retornada.</span><span class="sxs-lookup"><span data-stu-id="69189-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="69189-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="69189-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="69189-142">bota Ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) que contém a versão, o componente e informações de contexto de um erro.</span><span class="sxs-lookup"><span data-stu-id="69189-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="69189-143">O parâmetro _lppMAPIError_ é definido como NULL se nenhuma estrutura **MAPIERROR** for retornada.</span><span class="sxs-lookup"><span data-stu-id="69189-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69189-144">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="69189-144">Return value</span></span>

<span data-ttu-id="69189-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="69189-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69189-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="69189-146">Remarks</span></span>

<span data-ttu-id="69189-147">MAPI usa a função **HrValidateIPMSubtree** internamente para construir a subárvore IPM padrão em um repositório de mensagens quando o repositório é aberto pela primeira vez ou quando um repositório é tornado o repositório padrão.</span><span class="sxs-lookup"><span data-stu-id="69189-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="69189-148">Essa função também pode ser usada por aplicativos cliente para validar ou reparar pastas de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="69189-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="69189-149">O **HrValidateIPMSubtree** sempre cria as pastas de subárvores de pesquisa e de raiz IPM na pasta raiz do repositório e na pasta itens excluídos na pasta IPM Tree.</span><span class="sxs-lookup"><span data-stu-id="69189-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="69189-150">A pasta de sub-árvore IPM é a raiz da hierarquia IPM no repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="69189-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="69189-151">A pasta raiz de pesquisa pode ser usada como a raiz de uma subárvore para pastas de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="69189-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="69189-152">Os clientes IPM devem exibir o modo de exibição de pastas começando na pasta raiz da sub-árvore IPM e mostrando as pastas filhas abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="69189-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="69189-153">As informações na pasta raiz de um repositório de mensagens não devem aparecer na interface de usuário de um cliente.</span><span class="sxs-lookup"><span data-stu-id="69189-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="69189-154">Essa funcionalidade significa que, se um cliente deve ocultar informações, as informações podem ser colocadas no diretório raiz da sub-árvore IPM, onde não fica visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="69189-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="69189-155">Por outro lado, aplicativos não-IPM que exigem mensagens e pastas invisíveis para o usuário, por exemplo, em um repositório de mensagens baseado em servidor, podem colocá-los fora da hierarquia IPM.</span><span class="sxs-lookup"><span data-stu-id="69189-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="69189-156">**HrValidateIPMSubtree** define a propriedade **PR_VALID_FOLDER_MASK** para indicar se cada pasta IPM que ele cria tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="69189-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="69189-157">As seguintes propriedades de identificador de entrada do repositório de mensagens são definidas para os identificadores de entrada das pastas correspondentes e retornadas no parâmetro _lppProps_ juntamente com **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="69189-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="69189-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="69189-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="69189-165">Uma [PROP_TAG](prop_tag.md) de espaço reservado para a caixa de entrada IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="69189-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="69189-166">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69189-166">MFCMAPI reference</span></span>

<span data-ttu-id="69189-167">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="69189-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="69189-168">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="69189-168">**File**</span></span>|<span data-ttu-id="69189-169">**Função**</span><span class="sxs-lookup"><span data-stu-id="69189-169">**Function**</span></span>|<span data-ttu-id="69189-170">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="69189-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="69189-171">MstStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="69189-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="69189-172">CMsgStoreDlg:: OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="69189-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="69189-173">MFCMAPI usa o método **HrValidateIPMSubtree** para adicionar pastas padrão a um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="69189-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69189-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="69189-174">See also</span></span>



[<span data-ttu-id="69189-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="69189-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="69189-176">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="69189-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


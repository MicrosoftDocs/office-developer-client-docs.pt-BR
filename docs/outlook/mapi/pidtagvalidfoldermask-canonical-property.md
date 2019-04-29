---
title: Propriedade canônica PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427791"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="3e8aa-103">Propriedade canônica PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="3e8aa-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="3e8aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e8aa-105">Contém uma bitmask de sinalizadores que indicam a validade dos identificadores de entrada das pastas em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3e8aa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3e8aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e8aa-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="3e8aa-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="3e8aa-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e8aa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e8aa-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="3e8aa-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="3e8aa-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e8aa-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e8aa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3e8aa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3e8aa-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e8aa-112">Area:</span></span>  <br/> |<span data-ttu-id="3e8aa-113">Repositório de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8aa-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e8aa-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e8aa-114">Remarks</span></span>

<span data-ttu-id="3e8aa-115">Um identificador de entrada de pasta pode se tornar inválido se um usuário excluir a pasta ou se o repositório de mensagens ficar corrompido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="3e8aa-116">Um ou mais dos seguintes sinalizadores podem ser definidos para a bitmask:</span><span class="sxs-lookup"><span data-stu-id="3e8aa-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="3e8aa-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-118">A pasta Common views tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-119">ConFira **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="3e8aa-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-121">A pasta Finder tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-122">ConFira **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="3e8aa-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-124">A pasta de recebimento de mensagem interpessoal (IPM) tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-125">Consulte [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="3e8aa-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-127">A pasta de saída IPM tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-128">ConFira **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="3e8aa-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-130">A pasta Itens enviados IPM tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-131">ConFira **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="3e8aa-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-133">A subárvore de pastas IPM tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-134">ConFira **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="3e8aa-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-136">A pasta de itens excluídos IPM tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-137">ConFira **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="3e8aa-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="3e8aa-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="3e8aa-139">A pasta views tem um identificador de entrada válido.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="3e8aa-140">ConFira **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e8aa-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3e8aa-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e8aa-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3e8aa-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e8aa-142">Header files</span></span>

<span data-ttu-id="3e8aa-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3e8aa-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e8aa-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e8aa-145">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3e8aa-145">Mapitags.h</span></span>
  
> <span data-ttu-id="3e8aa-146">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3e8aa-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e8aa-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e8aa-147">See also</span></span>



[<span data-ttu-id="3e8aa-148">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8aa-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e8aa-149">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8aa-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e8aa-150">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3e8aa-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e8aa-151">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3e8aa-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


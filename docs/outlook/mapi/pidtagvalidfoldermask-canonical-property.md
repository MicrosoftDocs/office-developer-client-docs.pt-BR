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
ms.openlocfilehash: 605e2f528ea0afc1a35348320abaffeb142d9921
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590719"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="8bd28-103">Propriedade canônica PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="8bd28-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="8bd28-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd28-105">Contém uma bitmask dos sinalizadores que indicam a validade dos identificadores de entrada das pastas em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8bd28-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bd28-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8bd28-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bd28-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="8bd28-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="8bd28-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8bd28-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bd28-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="8bd28-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="8bd28-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8bd28-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bd28-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8bd28-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8bd28-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8bd28-112">Area:</span></span>  <br/> |<span data-ttu-id="8bd28-113">Armazenamento de mensagens MAPI</span><span class="sxs-lookup"><span data-stu-id="8bd28-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bd28-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bd28-114">Remarks</span></span>

<span data-ttu-id="8bd28-115">Identificador de entrada de uma pasta pode se tornar inválido se um usuário exclui a pasta ou se o armazenamento de mensagens for corrompido.</span><span class="sxs-lookup"><span data-stu-id="8bd28-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="8bd28-116">Um ou mais dos seguintes sinalizadores podem ser definido para a máscara de bits:</span><span class="sxs-lookup"><span data-stu-id="8bd28-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="8bd28-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="8bd28-118">A pasta de modos de exibição comuns tem um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-119">Consulte **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8bd28-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="8bd28-121">A pasta finder possui um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-122">Consulte **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="8bd28-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="8bd28-124">Receber a mensagem interpessoais (IPM) pasta tem um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-125">Consulte [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="8bd28-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="8bd28-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="8bd28-127">A pasta caixa de saída IPM possui um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-128">Consulte **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="8bd28-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="8bd28-130">A pasta Itens enviados do IPM possui um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-131">Consulte **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8bd28-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="8bd28-133">Subárvore IPM pasta possui um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-134">Consulte **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8bd28-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="8bd28-136">A pasta Itens excluídos do IPM possui um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-137">Consulte **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="8bd28-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="8bd28-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="8bd28-139">A pasta de modos de exibição tem um identificador de entrada válida.</span><span class="sxs-lookup"><span data-stu-id="8bd28-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="8bd28-140">Consulte **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8bd28-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="8bd28-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bd28-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8bd28-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8bd28-142">Header files</span></span>

<span data-ttu-id="8bd28-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bd28-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bd28-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8bd28-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bd28-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bd28-145">Mapitags.h</span></span>
  
> <span data-ttu-id="8bd28-146">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8bd28-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bd28-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bd28-147">See also</span></span>



[<span data-ttu-id="8bd28-148">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8bd28-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bd28-149">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8bd28-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bd28-150">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8bd28-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bd28-151">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8bd28-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


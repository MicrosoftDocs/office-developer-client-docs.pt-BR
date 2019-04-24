---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329488"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="06d98-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="06d98-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="06d98-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06d98-105">Realiza operações nas mensagens e subpastas em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="06d98-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="06d98-106">Header file:</span></span>  <br/> |<span data-ttu-id="06d98-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="06d98-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="06d98-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="06d98-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="06d98-109">Objetos Folder</span><span class="sxs-lookup"><span data-stu-id="06d98-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="06d98-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="06d98-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="06d98-111">Provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="06d98-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="06d98-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="06d98-112">Called by:</span></span>  <br/> |<span data-ttu-id="06d98-113">Aplicativos cliente e MAPI</span><span class="sxs-lookup"><span data-stu-id="06d98-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="06d98-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="06d98-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="06d98-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="06d98-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="06d98-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="06d98-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="06d98-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="06d98-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="06d98-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="06d98-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="06d98-119">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="06d98-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="06d98-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="06d98-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="06d98-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="06d98-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="06d98-122">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="06d98-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="06d98-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="06d98-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="06d98-124">Copia ou move uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="06d98-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="06d98-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="06d98-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="06d98-126">Exclui uma ou mais mensagens.</span><span class="sxs-lookup"><span data-stu-id="06d98-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="06d98-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="06d98-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="06d98-128">Cria uma nova subpasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="06d98-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="06d98-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="06d98-130">Copia ou move uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="06d98-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="06d98-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="06d98-132">Exclui uma subpasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="06d98-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="06d98-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="06d98-134">Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais das mensagens da pasta e gerencia o envio de relatórios de leitura.</span><span class="sxs-lookup"><span data-stu-id="06d98-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="06d98-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="06d98-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="06d98-136">Obtém o status associado a uma mensagem em uma pasta específica.</span><span class="sxs-lookup"><span data-stu-id="06d98-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="06d98-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="06d98-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="06d98-138">Define o status associado a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="06d98-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="06d98-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="06d98-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="06d98-140">Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="06d98-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="06d98-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="06d98-142">Exclui todas as mensagens e subpastas de uma pasta sem excluir a própria pasta.</span><span class="sxs-lookup"><span data-stu-id="06d98-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="06d98-143">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="06d98-143">**Required properties**</span></span>|<span data-ttu-id="06d98-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="06d98-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06d98-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="06d98-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="06d98-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="06d98-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-150">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="06d98-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="06d98-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="06d98-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="06d98-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-156">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="06d98-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="06d98-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="06d98-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="06d98-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="06d98-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06d98-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="06d98-161">See also</span></span>



[<span data-ttu-id="06d98-162">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="06d98-162">MAPI Interfaces</span></span>](mapi-interfaces.md)


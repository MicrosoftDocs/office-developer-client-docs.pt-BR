---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ed17fd7f826432da9460fe01e5aa76802726bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584629"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="1c23b-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1c23b-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="1c23b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c23b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c23b-105">Fornece acesso às informações do repositório de mensagem e mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="1c23b-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c23b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1c23b-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c23b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c23b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1c23b-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="1c23b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1c23b-109">Objeto de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="1c23b-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="1c23b-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="1c23b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c23b-111">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="1c23b-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1c23b-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="1c23b-112">Called by:</span></span>  <br/> |<span data-ttu-id="1c23b-113">Aplicativos de cliente, o spooler MAPI e MAPI</span><span class="sxs-lookup"><span data-stu-id="1c23b-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="1c23b-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="1c23b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1c23b-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="1c23b-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="1c23b-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="1c23b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1c23b-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="1c23b-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="1c23b-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="1c23b-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="1c23b-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="1c23b-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1c23b-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="1c23b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1c23b-121">Aviso</span><span class="sxs-lookup"><span data-stu-id="1c23b-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="1c23b-122">Registra para receber notificações de eventos especificados que afetam o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c23b-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="1c23b-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="1c23b-124">Cancela o envio de notificações configuradas anteriormente com uma chamada ao método **IMsgStore::Advise** .</span><span class="sxs-lookup"><span data-stu-id="1c23b-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1c23b-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="1c23b-126">Compara dois identificadores de entrada para determinar se eles se referem a mesma entrada em um repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c23b-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1c23b-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="1c23b-128">Abre uma pasta ou uma mensagem e retorna um ponteiro de interface para obter mais acesso.</span><span class="sxs-lookup"><span data-stu-id="1c23b-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="1c23b-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="1c23b-130">Estabelece uma pasta como destino para mensagens recebidas de uma classe de mensagem específica.</span><span class="sxs-lookup"><span data-stu-id="1c23b-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="1c23b-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="1c23b-132">Obtém a pasta que foi estabelecida como pasta para o armazenamento de mensagens de recebimento de destino para mensagens recebidas de uma classe de mensagem especificada ou como padrão.</span><span class="sxs-lookup"><span data-stu-id="1c23b-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="1c23b-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="1c23b-134">Fornece acesso à tabela de pasta de recebimento, uma tabela com informações sobre todas as pastas de recebimento para o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c23b-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1c23b-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="1c23b-136">Habilita o logoff ordenado o armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c23b-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="1c23b-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="1c23b-138">Tenta remover uma mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="1c23b-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="1c23b-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="1c23b-140">Fornece acesso à tabela de fila saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1c23b-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="1c23b-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="1c23b-142">Bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c23b-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="1c23b-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="1c23b-144">Permite que o provedor de armazenamento de mensagem executar o processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="1c23b-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="1c23b-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="1c23b-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="1c23b-146">Informa o armazenamento de mensagens que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="1c23b-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="1c23b-147">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="1c23b-147">**Required properties**</span></span>|<span data-ttu-id="1c23b-148">**Nível de acesso**</span><span class="sxs-lookup"><span data-stu-id="1c23b-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c23b-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-150">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1c23b-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="1c23b-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-156">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-162">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="1c23b-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1c23b-164">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1c23b-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="1c23b-165">As propriedades a seguir são para repositórios de mensagem da mensagem interpessoais (IPM):</span><span class="sxs-lookup"><span data-stu-id="1c23b-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="1c23b-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c23b-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c23b-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c23b-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1c23b-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1c23b-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="1c23b-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="1c23b-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="1c23b-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c23b-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c23b-172">See also</span></span>



[<span data-ttu-id="1c23b-173">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1c23b-173">MAPI Properties</span></span>](mapi-properties.md)


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
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348717"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="1342e-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1342e-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="1342e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1342e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1342e-105">Fornece acesso a informações do repositório de mensagens e mensagens e pastas.</span><span class="sxs-lookup"><span data-stu-id="1342e-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1342e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1342e-106">Header file:</span></span>  <br/> |<span data-ttu-id="1342e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1342e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1342e-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="1342e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1342e-109">Objeto do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="1342e-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="1342e-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1342e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1342e-111">Provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="1342e-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="1342e-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1342e-112">Called by:</span></span>  <br/> |<span data-ttu-id="1342e-113">Aplicativos cliente, o spooler MAPI e o MAPI</span><span class="sxs-lookup"><span data-stu-id="1342e-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="1342e-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="1342e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1342e-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="1342e-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="1342e-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="1342e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1342e-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="1342e-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="1342e-118">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="1342e-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="1342e-119">Não-Transacted</span><span class="sxs-lookup"><span data-stu-id="1342e-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1342e-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="1342e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1342e-121">Utilizar</span><span class="sxs-lookup"><span data-stu-id="1342e-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="1342e-122">Registra para receber notificações de eventos específicos que afetam o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="1342e-123">Cancelar</span><span class="sxs-lookup"><span data-stu-id="1342e-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="1342e-124">Cancela o envio de notificações anteriormente configuradas com uma chamada para o método **IMsgStore:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="1342e-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="1342e-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="1342e-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="1342e-126">Compara dois identificadores de entrada para determinar se eles se referem à mesma entrada em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="1342e-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="1342e-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="1342e-128">Abre uma pasta ou mensagem e retorna um ponteiro de interface para acesso adicional.</span><span class="sxs-lookup"><span data-stu-id="1342e-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="1342e-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="1342e-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="1342e-130">Estabelece uma pasta como o destino de mensagens de entrada de uma determinada classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1342e-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="1342e-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="1342e-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="1342e-132">Obtém a pasta que foi estabelecida como o destino para mensagens de entrada de uma classe de mensagem especificada ou como a pasta de recebimento padrão para o repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="1342e-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="1342e-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="1342e-134">Fornece acesso à tabela de pastas de recebimento, uma tabela com informações sobre todas as pastas de recebimento do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="1342e-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="1342e-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="1342e-136">Permite o logoff ordenada do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="1342e-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="1342e-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="1342e-138">Tenta remover uma mensagem da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="1342e-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="1342e-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="1342e-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="1342e-140">Fornece acesso à tabela de fila de saída, uma tabela que tem informações sobre todas as mensagens na fila de saída do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1342e-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="1342e-141">SetLockstate</span><span class="sxs-lookup"><span data-stu-id="1342e-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="1342e-142">Bloqueia ou desbloqueia uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1342e-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="1342e-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="1342e-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="1342e-144">Permite que o provedor de repositório de mensagens realize o processamento em uma mensagem enviada.</span><span class="sxs-lookup"><span data-stu-id="1342e-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="1342e-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="1342e-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="1342e-146">Informa ao repositório de mensagens que uma nova mensagem chegou.</span><span class="sxs-lookup"><span data-stu-id="1342e-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="1342e-147">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="1342e-147">**Required properties**</span></span>|<span data-ttu-id="1342e-148">**Nível de acesso**</span><span class="sxs-lookup"><span data-stu-id="1342e-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1342e-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-150">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1342e-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="1342e-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-152">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-154">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-156">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-160">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-162">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="1342e-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1342e-164">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1342e-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="1342e-165">As propriedades a seguir são para repositórios de mensagens de mensagens interpessoais (IPM):</span><span class="sxs-lookup"><span data-stu-id="1342e-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="1342e-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1342e-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1342e-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1342e-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1342e-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="1342e-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="1342e-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="1342e-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="1342e-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1342e-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="1342e-172">See also</span></span>



[<span data-ttu-id="1342e-173">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1342e-173">MAPI Properties</span></span>](mapi-properties.md)


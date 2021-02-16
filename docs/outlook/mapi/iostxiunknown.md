---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431992"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="859b7-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="859b7-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="859b7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="859b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="859b7-105">Fornece métodos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="859b7-105">Provides synchronization methods.</span></span> <span data-ttu-id="859b7-106">Essa interface recupera as informações necessárias para replicar as alterações locais no servidor e nas alterações do servidor no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="859b7-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="859b7-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="859b7-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="859b7-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="859b7-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="859b7-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="859b7-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="859b7-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="859b7-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="859b7-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="859b7-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="859b7-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="859b7-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="859b7-113">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="859b7-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="859b7-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="859b7-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="859b7-115">Informa ao armazenamento local que a sincronização está prestes a iniciar.</span><span class="sxs-lookup"><span data-stu-id="859b7-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="859b7-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="859b7-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="859b7-117">Prepara o armazenamento local para sincronização em um estado específico e recupera as informações necessárias para replicar.</span><span class="sxs-lookup"><span data-stu-id="859b7-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="859b7-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="859b7-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="859b7-119">Encerra a sincronização no estado atual e sai desse estado.</span><span class="sxs-lookup"><span data-stu-id="859b7-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="859b7-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="859b7-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="859b7-121">Inicia a sincronização para um header de mensagem.</span><span class="sxs-lookup"><span data-stu-id="859b7-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="859b7-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="859b7-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="859b7-123">Encerra a sincronização para um header de mensagem.</span><span class="sxs-lookup"><span data-stu-id="859b7-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="859b7-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="859b7-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="859b7-125">Define o resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="859b7-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="859b7-126">*Membro placeholder*</span><span class="sxs-lookup"><span data-stu-id="859b7-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="859b7-127">*Sem suporte ou documentado.*</span><span class="sxs-lookup"><span data-stu-id="859b7-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="859b7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="859b7-128">Remarks</span></span>

<span data-ttu-id="859b7-129">Quando um cliente carrega ou sincroniza pastas e conteúdo de pastas em um armazenamento local, ele move o armazenamento local de um estado para outro, conforme ilustrado no diagrama de transição de estado em [Sobre](about-the-replication-state-machine.md)a Máquina de Estado de Replicação.</span><span class="sxs-lookup"><span data-stu-id="859b7-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="859b7-130">A seguir está a ordem dos eventos para o cliente mover o armazenamento local de um estado para outro:</span><span class="sxs-lookup"><span data-stu-id="859b7-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="859b7-131">O cliente chama **IOSTX::InitSync** para informar ao armazenamento local que a replicação está prestes a iniciar.</span><span class="sxs-lookup"><span data-stu-id="859b7-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="859b7-132">Dependendo da direção da replicação e dos objetos a replicar, o cliente chama **IOSTX::SyncBeg** para iniciar a replicação no estado apropriado.</span><span class="sxs-lookup"><span data-stu-id="859b7-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="859b7-133">O Outlook fornece ao cliente as informações necessárias, e o cliente executa a replicação.</span><span class="sxs-lookup"><span data-stu-id="859b7-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="859b7-134">O cliente chama **IOSTX::SetSyncResult** para retornar o resultado da replicação.</span><span class="sxs-lookup"><span data-stu-id="859b7-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="859b7-135">O cliente chama **IOSTX::SyncEnd** para encerrar a replicação, fornecendo ao Outlook as informações necessárias para a replicação subsequente.</span><span class="sxs-lookup"><span data-stu-id="859b7-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="859b7-136">Em particular, ao baixar itens de mensagem, o cliente usa **IOSTX::SyncHdrBeg** e **IOSTX::SyncHdrEnd** para atualizar um item de mensagem completo com o header da mensagem no armazenamento local:</span><span class="sxs-lookup"><span data-stu-id="859b7-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="859b7-137">Em **IOSTX::SyncHdrBeg**, o armazenamento local faz a transição para o estado do header da mensagem de download.</span><span class="sxs-lookup"><span data-stu-id="859b7-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="859b7-138">Inicialmente, o Outlook fornece ao cliente o header de mensagem atual no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="859b7-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="859b7-139">O cliente baixa um item de mensagem completo junto com o header da mensagem.</span><span class="sxs-lookup"><span data-stu-id="859b7-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="859b7-140">O Outlook atualiza o item no armazenamento local com o item de mensagem completo.</span><span class="sxs-lookup"><span data-stu-id="859b7-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="859b7-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="859b7-141">See also</span></span>



[<span data-ttu-id="859b7-142">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="859b7-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="859b7-143">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="859b7-143">MAPI Constants</span></span>](mapi-constants.md)


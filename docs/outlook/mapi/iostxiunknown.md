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
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767604"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="38db6-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38db6-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="38db6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38db6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38db6-105">Fornece os métodos de sincronização.</span><span class="sxs-lookup"><span data-stu-id="38db6-105">Provides synchronization methods.</span></span> <span data-ttu-id="38db6-106">Essa interface recupera as informações necessárias para replicar alterações locais para o servidor e as alterações no repositório local no servidor.</span><span class="sxs-lookup"><span data-stu-id="38db6-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38db6-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="38db6-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="38db6-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="38db6-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="38db6-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="38db6-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="38db6-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="38db6-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="38db6-111">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="38db6-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="38db6-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="38db6-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="38db6-113">Obtém informações estendidas sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="38db6-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="38db6-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="38db6-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="38db6-115">Informa o armazenamento local que sincronização está prestes a iniciar.</span><span class="sxs-lookup"><span data-stu-id="38db6-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="38db6-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="38db6-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="38db6-117">Prepara o armazenamento local para sincronização em um estado particular e recupera as informações necessárias para replicar.</span><span class="sxs-lookup"><span data-stu-id="38db6-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="38db6-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="38db6-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="38db6-119">Finaliza a sincronização no estado atual e sai desse estado.</span><span class="sxs-lookup"><span data-stu-id="38db6-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="38db6-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="38db6-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="38db6-121">Inicia a sincronização de um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="38db6-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="38db6-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="38db6-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="38db6-123">Finaliza a sincronização para um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="38db6-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="38db6-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="38db6-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="38db6-125">Define o resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="38db6-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="38db6-126">*Membro do espaço reservado*</span><span class="sxs-lookup"><span data-stu-id="38db6-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="38db6-127">*Não tem suporte ou documentadas.*</span><span class="sxs-lookup"><span data-stu-id="38db6-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38db6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="38db6-128">Remarks</span></span>

<span data-ttu-id="38db6-129">Quando um cliente carrega ou sincroniza pastas e o conteúdo da pasta em um repositório local, ele transfere o armazenamento local de um estado para outro conforme ilustrado no diagrama a transição de estado no [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="38db6-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="38db6-130">Este é a ordem de eventos para o cliente mover o repositório local de um estado para outro:</span><span class="sxs-lookup"><span data-stu-id="38db6-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="38db6-131">O cliente chama **IOSTX::InitSync** para informar o armazenamento local que a replicação está prestes a iniciar.</span><span class="sxs-lookup"><span data-stu-id="38db6-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="38db6-132">Dependendo da direção da replicação e os objetos para replicar, o cliente chama **IOSTX::SyncBeg** para começar a replicação em um estado apropriado.</span><span class="sxs-lookup"><span data-stu-id="38db6-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="38db6-133">O Outlook oferece o cliente as informações necessárias e o cliente executa a replicação.</span><span class="sxs-lookup"><span data-stu-id="38db6-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="38db6-134">O cliente chama **IOSTX::SetSyncResult** para retornar o resultado da replicação.</span><span class="sxs-lookup"><span data-stu-id="38db6-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="38db6-135">O cliente chama **IOSTX::SyncEnd** para encerrar a replicação, fornecendo Outlook as informações necessárias para replicação subsequentes.</span><span class="sxs-lookup"><span data-stu-id="38db6-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="38db6-136">Em particular, ao fazer o download de itens de mensagem, o cliente usa **IOSTX::SyncHdrBeg** e **IOSTX::SyncHdrEnd** para atualizar um item de mensagem completo com o cabeçalho da mensagem no armazenamento local:</span><span class="sxs-lookup"><span data-stu-id="38db6-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="38db6-137">Após a **IOSTX::SyncHdrBeg**, o local armazenar transições para o estado de cabeçalho de mensagem do download.</span><span class="sxs-lookup"><span data-stu-id="38db6-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="38db6-138">Inicialmente, o Outlook fornece ao cliente com o cabeçalho da mensagem atual no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="38db6-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="38db6-139">O cliente baixa um item de mensagem completa em conjunto com o cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="38db6-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="38db6-140">Outlook atualiza o item no armazenamento local com o item de mensagem completa.</span><span class="sxs-lookup"><span data-stu-id="38db6-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38db6-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="38db6-141">See also</span></span>



[<span data-ttu-id="38db6-142">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="38db6-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="38db6-143">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="38db6-143">MAPI Constants</span></span>](mapi-constants.md)


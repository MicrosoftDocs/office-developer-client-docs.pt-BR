---
title: IOSTXSyncBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411936"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="b437f-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b437f-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="b437f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b437f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b437f-105">Prepara o armazenamento local para sincronização em um estado específico e recupera as informações necessárias para replicar.</span><span class="sxs-lookup"><span data-stu-id="b437f-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="b437f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b437f-106">Parameters</span></span>

 <span data-ttu-id="b437f-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="b437f-107">_uiSync_</span></span>
  
>  <span data-ttu-id="b437f-108">[in] O estado em que o armazenamento local entrará.</span><span class="sxs-lookup"><span data-stu-id="b437f-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="b437f-109">A seguir está uma lista de identificadodores de estado:</span><span class="sxs-lookup"><span data-stu-id="b437f-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="b437f-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="b437f-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="b437f-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="b437f-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="b437f-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="b437f-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="b437f-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="b437f-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="b437f-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="b437f-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="b437f-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="b437f-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="b437f-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b437f-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="b437f-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="b437f-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="b437f-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="b437f-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="b437f-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="b437f-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="b437f-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="b437f-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="b437f-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="b437f-121">_ppv_</span></span>
  
>  <span data-ttu-id="b437f-122">[in]/[out] Ponteiro para a estrutura de dados correspondente ao estado a inserir.</span><span class="sxs-lookup"><span data-stu-id="b437f-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="b437f-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="b437f-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="b437f-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="b437f-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="b437f-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="b437f-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="b437f-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="b437f-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="b437f-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="b437f-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="b437f-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="b437f-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="b437f-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="b437f-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="b437f-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="b437f-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="b437f-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="b437f-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="b437f-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="b437f-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="b437f-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="b437f-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="b437f-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="b437f-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="b437f-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="b437f-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="b437f-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="b437f-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="b437f-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="b437f-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="b437f-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="b437f-138">Remarks</span></span>

<span data-ttu-id="b437f-139">O cliente chama **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** para definir o resultado da sincronização e chama **[IOSTX::SyncEnd](iostx-syncend.md)** para encerrar esse estado.</span><span class="sxs-lookup"><span data-stu-id="b437f-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="b437f-140">O cliente deve chamar **[IOSTX::SyncEnd](iostx-syncend.md)** para cada chamada para **IOSTX::SyncBeg** para determinar se o estado foi replicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b437f-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="b437f-141">Depois que isso é determinado, o Outlook pode começar a limpar seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="b437f-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="b437f-142">A maioria dessas estruturas contém informações [out]/[in], permitindo que o Outlook passe informações para o cliente e o cliente para passar informações para o Outlook.</span><span class="sxs-lookup"><span data-stu-id="b437f-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="b437f-143">Quando o cliente chama **IOSTX::SyncBeg**, o Outlook aloca a estrutura de dados para um determinado estado e a inicializa com informações para esse estado.</span><span class="sxs-lookup"><span data-stu-id="b437f-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="b437f-144">Essas são as informações [out].</span><span class="sxs-lookup"><span data-stu-id="b437f-144">This is the [out] information.</span></span> <span data-ttu-id="b437f-145">Enquanto estiver em um estado, o cliente atualiza a estrutura de dados correspondente para esse estado.</span><span class="sxs-lookup"><span data-stu-id="b437f-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="b437f-146">Essas são as informações [in].</span><span class="sxs-lookup"><span data-stu-id="b437f-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b437f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b437f-147">See also</span></span>



[<span data-ttu-id="b437f-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b437f-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b437f-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b437f-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="b437f-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b437f-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b437f-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b437f-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="b437f-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b437f-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b437f-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b437f-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="b437f-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b437f-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b437f-155">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="b437f-155">MAPI Constants</span></span>](mapi-constants.md)


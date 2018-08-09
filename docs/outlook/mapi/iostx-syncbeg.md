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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ddc61aa42b1087ed5f0ecb7986125ceef27cddce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767577"
---
# <a name="iostxsyncbeg"></a><span data-ttu-id="a862d-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="a862d-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="a862d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a862d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a862d-105">Prepara o armazenamento local para sincronização em um estado particular e recupera as informações necessárias para replicar.</span><span class="sxs-lookup"><span data-stu-id="a862d-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="a862d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a862d-106">Parameters</span></span>

 <span data-ttu-id="a862d-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="a862d-107">_uiSync_</span></span>
  
>  <span data-ttu-id="a862d-108">[in] O estado que entrará no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="a862d-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="a862d-109">A seguir está uma lista de identificadores de estado:</span><span class="sxs-lookup"><span data-stu-id="a862d-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="a862d-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="a862d-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="a862d-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="a862d-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="a862d-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="a862d-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="a862d-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="a862d-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="a862d-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="a862d-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="a862d-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="a862d-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="a862d-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a862d-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="a862d-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="a862d-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="a862d-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="a862d-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="a862d-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="a862d-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="a862d-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="a862d-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="a862d-121">_ppv_</span><span class="sxs-lookup"><span data-stu-id="a862d-121">_ppv_</span></span>
  
>  <span data-ttu-id="a862d-122">[in] / [ponteiro para a estrutura de dados correspondente ao estado insiram out].</span><span class="sxs-lookup"><span data-stu-id="a862d-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="a862d-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="a862d-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="a862d-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="a862d-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="a862d-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="a862d-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="a862d-126">SYNC</span><span class="sxs-lookup"><span data-stu-id="a862d-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="a862d-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="a862d-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="a862d-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="a862d-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="a862d-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="a862d-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="a862d-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="a862d-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="a862d-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="a862d-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="a862d-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="a862d-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="a862d-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="a862d-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="a862d-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="a862d-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="a862d-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="a862d-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="a862d-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="a862d-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="a862d-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="a862d-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="a862d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="a862d-138">Remarks</span></span>

<span data-ttu-id="a862d-139">O cliente chama **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** para definir o resultado da sincronização e, em seguida, chama **[IOSTX::SyncEnd](iostx-syncend.md)** para encerrar a esse estado.</span><span class="sxs-lookup"><span data-stu-id="a862d-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="a862d-140">O cliente deve chamar **[IOSTX::SyncEnd](iostx-syncend.md)** para cada chamada ao **IOSTX::SyncBeg** para determinar se o estado foi replicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="a862d-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="a862d-141">Depois que tiver sido determinado, o Outlook pode começar a limpar o seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="a862d-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="a862d-142">A maioria dessas estruturas contém [out] / [in] informações, permitindo que o Outlook passar informações para o cliente e o cliente para passar informações para o Outlook.</span><span class="sxs-lookup"><span data-stu-id="a862d-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="a862d-143">Quando o cliente chama **IOSTX::SyncBeg**, Outlook aloca a estrutura de dados para um determinado estado e inicializa com informações para esse estado.</span><span class="sxs-lookup"><span data-stu-id="a862d-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="a862d-144">Essas são as informações de [out].</span><span class="sxs-lookup"><span data-stu-id="a862d-144">This is the [out] information.</span></span> <span data-ttu-id="a862d-145">Enquanto estiver em um estado, o cliente atualiza a estrutura de dados correspondente para esse estado.</span><span class="sxs-lookup"><span data-stu-id="a862d-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="a862d-146">Este é o [in] informações.</span><span class="sxs-lookup"><span data-stu-id="a862d-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a862d-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a862d-147">See also</span></span>



[<span data-ttu-id="a862d-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a862d-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="a862d-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="a862d-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="a862d-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="a862d-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="a862d-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="a862d-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="a862d-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="a862d-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="a862d-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="a862d-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="a862d-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a862d-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="a862d-155">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a862d-155">MAPI Constants</span></span>](mapi-constants.md)


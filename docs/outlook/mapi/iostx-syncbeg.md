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
# <a name="iostxsyncbeg"></a><span data-ttu-id="092ed-103">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="092ed-103">IOSTX::SyncBeg</span></span>

  
  
<span data-ttu-id="092ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="092ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="092ed-105">Prepara o repositório local para sincronização em um determinado Estado e recupera as informações necessárias para a replicação.</span><span class="sxs-lookup"><span data-stu-id="092ed-105">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="092ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="092ed-106">Parameters</span></span>

 <span data-ttu-id="092ed-107">_uiSync_</span><span class="sxs-lookup"><span data-stu-id="092ed-107">_uiSync_</span></span>
  
>  <span data-ttu-id="092ed-108">no O estado que o repositório local inserirá.</span><span class="sxs-lookup"><span data-stu-id="092ed-108">[in] The state that the local store will enter.</span></span> <span data-ttu-id="092ed-109">Veja a seguir uma lista de identificadores de Estado:</span><span class="sxs-lookup"><span data-stu-id="092ed-109">The following is a list of state identifers:</span></span> 
    
<span data-ttu-id="092ed-110">LR_SYNC_IDLE</span><span class="sxs-lookup"><span data-stu-id="092ed-110">LR_SYNC_IDLE</span></span>
  
> 
    
<span data-ttu-id="092ed-111">LR_SYNC</span><span class="sxs-lookup"><span data-stu-id="092ed-111">LR_SYNC</span></span>
  
> 
    
<span data-ttu-id="092ed-112">LR_SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="092ed-112">LR_SYNC_UPLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="092ed-113">LR_SYNC_UPLOAD_FOLDER</span><span class="sxs-lookup"><span data-stu-id="092ed-113">LR_SYNC_UPLOAD_FOLDER</span></span>
  
> 
    
<span data-ttu-id="092ed-114">LR_SYNC_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="092ed-114">LR_SYNC_CONTENTS</span></span>
  
> 
    
<span data-ttu-id="092ed-115">LR_SYNC_UPLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="092ed-115">LR_SYNC_UPLOAD_TABLE</span></span>
  
> 
    
<span data-ttu-id="092ed-116">LR_SYNC_UPLOAD_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="092ed-116">LR_SYNC_UPLOAD_MESSAGE</span></span>
  
> 
    
<span data-ttu-id="092ed-117">LR_SYNC_UPLOAD_MESSAGE_READ</span><span class="sxs-lookup"><span data-stu-id="092ed-117">LR_SYNC_UPLOAD_MESSAGE_READ</span></span>
  
> 
    
<span data-ttu-id="092ed-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span><span class="sxs-lookup"><span data-stu-id="092ed-118">LR_SYNC_UPLOAD_MESSAGE_DEL</span></span>
  
> 
    
<span data-ttu-id="092ed-119">LR_SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="092ed-119">LR_SYNC_DOWNLOAD_HIERARCHY</span></span>
  
> 
    
<span data-ttu-id="092ed-120">LR_SYNC_DOWNLOAD_TABLE</span><span class="sxs-lookup"><span data-stu-id="092ed-120">LR_SYNC_DOWNLOAD_TABLE</span></span>
  
> 
    
 <span data-ttu-id="092ed-121">_PPV_</span><span class="sxs-lookup"><span data-stu-id="092ed-121">_ppv_</span></span>
  
>  <span data-ttu-id="092ed-122">[in]/[out] ponteiro para a estrutura de dados que corresponde ao estado a ser inserido.</span><span class="sxs-lookup"><span data-stu-id="092ed-122">[in]/[out] Pointer to the data structure corresponding to the state to enter.</span></span> 
    
[<span data-ttu-id="092ed-123">DNHIER</span><span class="sxs-lookup"><span data-stu-id="092ed-123">DNHIER</span></span>](dnhier.md)
  
> 
    
[<span data-ttu-id="092ed-124">DNTBL</span><span class="sxs-lookup"><span data-stu-id="092ed-124">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="092ed-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="092ed-125">DNTBL</span></span>](dntbl.md)
  
> 
    
[<span data-ttu-id="092ed-126">SINCRONIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="092ed-126">SYNC</span></span>](sync.md)
  
> 
    
[<span data-ttu-id="092ed-127">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="092ed-127">SYNCCONT</span></span>](synccont.md)
  
> 
    
[<span data-ttu-id="092ed-128">UPDEL</span><span class="sxs-lookup"><span data-stu-id="092ed-128">UPDEL</span></span>](updel.md)
  
> 
    
[<span data-ttu-id="092ed-129">UPDELE</span><span class="sxs-lookup"><span data-stu-id="092ed-129">UPDELE</span></span>](updele.md)
  
> 
    
[<span data-ttu-id="092ed-130">UPFLD</span><span class="sxs-lookup"><span data-stu-id="092ed-130">UPFLD</span></span>](upfld.md)
  
> 
    
[<span data-ttu-id="092ed-131">UPHIER</span><span class="sxs-lookup"><span data-stu-id="092ed-131">UPHIER</span></span>](uphier.md)
  
> 
    
[<span data-ttu-id="092ed-132">UPMOV</span><span class="sxs-lookup"><span data-stu-id="092ed-132">UPMOV</span></span>](upmov.md)
  
> 
    
[<span data-ttu-id="092ed-133">UPMSG</span><span class="sxs-lookup"><span data-stu-id="092ed-133">UPMSG</span></span>](upmsg.md)
  
> 
    
[<span data-ttu-id="092ed-134">UPREAD</span><span class="sxs-lookup"><span data-stu-id="092ed-134">UPREAD</span></span>](upread.md)
  
> 
    
[<span data-ttu-id="092ed-135">UPREADE</span><span class="sxs-lookup"><span data-stu-id="092ed-135">UPREADE</span></span>](upreade.md)
  
> 
    
[<span data-ttu-id="092ed-136">UPTBL</span><span class="sxs-lookup"><span data-stu-id="092ed-136">UPTBL</span></span>](uptbl.md)
  
> 
    
[<span data-ttu-id="092ed-137">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="092ed-137">UPTBLE</span></span>](uptble.md)
  
> 
    
## <a name="remarks"></a><span data-ttu-id="092ed-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="092ed-138">Remarks</span></span>

<span data-ttu-id="092ed-139">O cliente chama **[IOSTX:: SetSyncResult](iostx-setsyncresult.md)** para definir o resultado da sincronização e, em seguida, chama **[IOSTX:: SyncEnd](iostx-syncend.md)** para terminar esse estado.</span><span class="sxs-lookup"><span data-stu-id="092ed-139">The client calls **[IOSTX::SetSyncResult](iostx-setsyncresult.md)** to set the result of the synchronization, and then calls **[IOSTX::SyncEnd](iostx-syncend.md)** to end that state.</span></span> <span data-ttu-id="092ed-140">O cliente deve chamar **[IOSTX:: SyncEnd](iostx-syncend.md)** para cada chamada para **IOSTX:: SyncBeg** a fim de determinar se o estado foi replicado com êxito.</span><span class="sxs-lookup"><span data-stu-id="092ed-140">The client must call **[IOSTX::SyncEnd](iostx-syncend.md)** for each call to **IOSTX::SyncBeg** in order to determine whether the state has been successfully replicated.</span></span> <span data-ttu-id="092ed-141">Depois de determinado, o Outlook pode começar a limpar seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="092ed-141">Once this has been determined, Outlook can begin to clean up its internal state.</span></span> 
  
<span data-ttu-id="092ed-142">A maioria dessas estruturas contém informações de [out]/[in], permitindo que o Outlook passe informações para o cliente e o cliente passe informações para o Outlook.</span><span class="sxs-lookup"><span data-stu-id="092ed-142">Most of these structures contain [out]/[in] information, allowing Outlook to pass information to the client, and the client to pass information to Outlook.</span></span> <span data-ttu-id="092ed-143">Quando o cliente chama **IOSTX:: SyncBeg**, o Outlook aloca a estrutura de dados para um determinado Estado e a inicializa com informações para esse estado.</span><span class="sxs-lookup"><span data-stu-id="092ed-143">When the client calls **IOSTX::SyncBeg**, Outlook allocates the data structure for a given state and initializes it with information for that state.</span></span> <span data-ttu-id="092ed-144">Estas são as informações de [out].</span><span class="sxs-lookup"><span data-stu-id="092ed-144">This is the [out] information.</span></span> <span data-ttu-id="092ed-145">Enquanto estiver em um estado, o cliente atualiza a estrutura de dados correspondente para esse estado.</span><span class="sxs-lookup"><span data-stu-id="092ed-145">While in a state, the client updates the corresponding data structure for that state.</span></span> <span data-ttu-id="092ed-146">Estas são as informações do [in].</span><span class="sxs-lookup"><span data-stu-id="092ed-146">This is the [in] information.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="092ed-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="092ed-147">See also</span></span>



[<span data-ttu-id="092ed-148">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="092ed-148">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="092ed-149">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="092ed-149">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="092ed-150">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="092ed-150">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="092ed-151">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="092ed-151">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="092ed-152">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="092ed-152">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="092ed-153">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="092ed-153">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="092ed-154">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="092ed-154">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="092ed-155">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="092ed-155">MAPI Constants</span></span>](mapi-constants.md)


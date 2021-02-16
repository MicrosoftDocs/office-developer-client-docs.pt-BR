---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418705"
---
# <a name="mapisib"></a><span data-ttu-id="eb2e8-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="eb2e8-103">MAPISIB</span></span>

  
  
<span data-ttu-id="eb2e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb2e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb2e8-105">Essa estrutura é usada com [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="eb2e8-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="eb2e8-106">Members</span><span class="sxs-lookup"><span data-stu-id="eb2e8-106">Members</span></span>

 <span data-ttu-id="eb2e8-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="eb2e8-107">**ulSize**</span></span>
  
> <span data-ttu-id="eb2e8-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-108">The size of the structure.</span></span>
    
 <span data-ttu-id="eb2e8-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="eb2e8-109">**ulFlags**</span></span>
  
> <span data-ttu-id="eb2e8-110">Um sinalizador que indica o tipo de sincronização. Deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="eb2e8-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="eb2e8-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="eb2e8-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="eb2e8-112">0x00000200</span></span>  <br/> |<span data-ttu-id="eb2e8-113">Envie a mensagem para o servidor (não está em uso no momento).</span><span class="sxs-lookup"><span data-stu-id="eb2e8-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="eb2e8-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="eb2e8-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="eb2e8-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="eb2e8-115">0x00000001</span></span>  <br/> |<span data-ttu-id="eb2e8-116">Push hierarchy changes to the server.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="eb2e8-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="eb2e8-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="eb2e8-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="eb2e8-118">0x00000002</span></span>  <br/> |<span data-ttu-id="eb2e8-119">Pull hierarchy changes from server.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="eb2e8-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="eb2e8-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="eb2e8-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="eb2e8-121">0x00000040</span></span>  <br/> |<span data-ttu-id="eb2e8-122">Enviar alterações de mensagem por push para o servidor.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="eb2e8-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="eb2e8-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="eb2e8-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="eb2e8-124">0x00000080</span></span>  <br/> |<span data-ttu-id="eb2e8-125">Pull message changes from server.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="eb2e8-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="eb2e8-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="eb2e8-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="eb2e8-127">0x20000000</span></span>  <br/> |<span data-ttu-id="eb2e8-128">A sincronização foi iniciada pelo usuário e deve ter uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="eb2e8-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="eb2e8-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="eb2e8-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="eb2e8-130">0x02000000</span></span>  <br/> |<span data-ttu-id="eb2e8-131">Deve sincronizar apenas os headers e não corpos completos.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="eb2e8-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="eb2e8-132">**psesSync**</span></span>
  
> <span data-ttu-id="eb2e8-133">[IN] Um ponteiro para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="eb2e8-134">**callBack**</span><span class="sxs-lookup"><span data-stu-id="eb2e8-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="eb2e8-135">[IN] Um ponteiro para a interface na qual fornecer o progresso.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="eb2e8-136">Ele pode ser usado para consultar a interface de [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="eb2e8-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="eb2e8-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="eb2e8-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="eb2e8-138">[OUT] O evento que ocorrerá quando o thread que acabou de ser criado for concluído.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="eb2e8-139">O ponteiro deve ser válido porque conterá o evento.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb2e8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb2e8-140">See also</span></span>



[<span data-ttu-id="eb2e8-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb2e8-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="eb2e8-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb2e8-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


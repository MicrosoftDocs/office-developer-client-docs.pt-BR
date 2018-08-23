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
ms.openlocfilehash: f696d9739014659812de3309ec885f37a6f85cc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572134"
---
# <a name="mapisib"></a><span data-ttu-id="844bd-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="844bd-103">MAPISIB</span></span>

  
  
<span data-ttu-id="844bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="844bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="844bd-105">Essa estrutura é usada com [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="844bd-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="844bd-106">Members</span><span class="sxs-lookup"><span data-stu-id="844bd-106">Members</span></span>

 <span data-ttu-id="844bd-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="844bd-107">**ulSize**</span></span>
  
> <span data-ttu-id="844bd-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="844bd-108">The size of the structure.</span></span>
    
 <span data-ttu-id="844bd-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="844bd-109">**ulFlags**</span></span>
  
> <span data-ttu-id="844bd-110">Um sinalizador que indica o tipo de sincronização. Ele deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="844bd-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="844bd-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="844bd-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="844bd-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="844bd-112">0x00000200</span></span>  <br/> |<span data-ttu-id="844bd-113">Envie a mensagem para o servidor (não está atualmente em uso).</span><span class="sxs-lookup"><span data-stu-id="844bd-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="844bd-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="844bd-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="844bd-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="844bd-115">0x00000001</span></span>  <br/> |<span data-ttu-id="844bd-116">Hierarquia de push altera para o servidor.</span><span class="sxs-lookup"><span data-stu-id="844bd-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="844bd-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="844bd-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="844bd-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="844bd-118">0x00000002</span></span>  <br/> |<span data-ttu-id="844bd-119">Retire as alterações de hierarquia do servidor.</span><span class="sxs-lookup"><span data-stu-id="844bd-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="844bd-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="844bd-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="844bd-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="844bd-121">0x00000040</span></span>  <br/> |<span data-ttu-id="844bd-122">Enviar mensagem for alterado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="844bd-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="844bd-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="844bd-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="844bd-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="844bd-124">0x00000080</span></span>  <br/> |<span data-ttu-id="844bd-125">Receba a mensagem é alterado do servidor.</span><span class="sxs-lookup"><span data-stu-id="844bd-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="844bd-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="844bd-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="844bd-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="844bd-127">0x20000000</span></span>  <br/> |<span data-ttu-id="844bd-128">A sincronização foi iniciada pelo usuário e deve ser uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="844bd-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="844bd-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="844bd-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="844bd-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="844bd-130">0x02000000</span></span>  <br/> |<span data-ttu-id="844bd-131">Só deve sincronizar cabeçalhos e corpos não está cheio.</span><span class="sxs-lookup"><span data-stu-id="844bd-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="844bd-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="844bd-132">**psesSync**</span></span>
  
> <span data-ttu-id="844bd-133">[IN] Um ponteiro para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="844bd-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="844bd-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="844bd-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="844bd-135">[IN] Um ponteiro para a interface no qual você deseja fornecer o progresso.</span><span class="sxs-lookup"><span data-stu-id="844bd-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="844bd-136">Ele pode ser usado para consultar a interface para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="844bd-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="844bd-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="844bd-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="844bd-138">[OUT] O evento que ocorrerá quando o segmento que acabou de ser criado for concluído.</span><span class="sxs-lookup"><span data-stu-id="844bd-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="844bd-139">O ponteiro deve ser válido, pois ele conterá o evento.</span><span class="sxs-lookup"><span data-stu-id="844bd-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="844bd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="844bd-140">See also</span></span>



[<span data-ttu-id="844bd-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="844bd-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="844bd-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="844bd-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


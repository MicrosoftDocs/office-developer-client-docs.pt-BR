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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270207"
---
# <a name="mapisib"></a><span data-ttu-id="562ff-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="562ff-103">MAPISIB</span></span>

  
  
<span data-ttu-id="562ff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="562ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="562ff-105">Essa estrutura é usada com [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="562ff-106">Members</span><span class="sxs-lookup"><span data-stu-id="562ff-106">Members</span></span>

 <span data-ttu-id="562ff-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="562ff-107">**ulSize**</span></span>
  
> <span data-ttu-id="562ff-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="562ff-108">The size of the structure.</span></span>
    
 <span data-ttu-id="562ff-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="562ff-109">**ulFlags**</span></span>
  
> <span data-ttu-id="562ff-110">Um sinalizador que indica o tipo de sincronização. Deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="562ff-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="562ff-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="562ff-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="562ff-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="562ff-112">0x00000200</span></span>  <br/> |<span data-ttu-id="562ff-113">Envie a mensagem para o servidor (não está em uso no momento).</span><span class="sxs-lookup"><span data-stu-id="562ff-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="562ff-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="562ff-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="562ff-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="562ff-115">0x00000001</span></span>  <br/> |<span data-ttu-id="562ff-116">Push as alterações de hierarquia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="562ff-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="562ff-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="562ff-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="562ff-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="562ff-118">0x00000002</span></span>  <br/> |<span data-ttu-id="562ff-119">Extrair alterações de hierarquia do servidor.</span><span class="sxs-lookup"><span data-stu-id="562ff-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="562ff-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="562ff-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="562ff-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="562ff-121">0x00000040</span></span>  <br/> |<span data-ttu-id="562ff-122">Alterações de mensagens por push no servidor.</span><span class="sxs-lookup"><span data-stu-id="562ff-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="562ff-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="562ff-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="562ff-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="562ff-124">0x00000080</span></span>  <br/> |<span data-ttu-id="562ff-125">As alterações de mensagem de recebimento do servidor.</span><span class="sxs-lookup"><span data-stu-id="562ff-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="562ff-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="562ff-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="562ff-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="562ff-127">0x20000000</span></span>  <br/> |<span data-ttu-id="562ff-128">A sincronização foi iniciada pelo usuário e deve ser uma prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="562ff-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="562ff-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="562ff-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="562ff-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="562ff-130">0x02000000</span></span>  <br/> |<span data-ttu-id="562ff-131">Só deve sincronizar cabeçalhos e não corpos completos.</span><span class="sxs-lookup"><span data-stu-id="562ff-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="562ff-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="562ff-132">**psesSync**</span></span>
  
> <span data-ttu-id="562ff-133">NO Um ponteiro para a sessão MAPI.</span><span class="sxs-lookup"><span data-stu-id="562ff-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="562ff-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="562ff-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="562ff-135">NO Um ponteiro para a interface na qual fornecer progresso.</span><span class="sxs-lookup"><span data-stu-id="562ff-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="562ff-136">Ele pode ser usado para consultar a interface para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="562ff-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="562ff-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="562ff-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="562ff-138">BOTA O evento que ocorrerá quando o thread que acabou de ser criado estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="562ff-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="562ff-139">O ponteiro deve ser válido, pois conterá o evento.</span><span class="sxs-lookup"><span data-stu-id="562ff-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="562ff-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="562ff-140">See also</span></span>



[<span data-ttu-id="562ff-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="562ff-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="562ff-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="562ff-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


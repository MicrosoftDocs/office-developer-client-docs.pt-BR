---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 07305f712fd925b206ce18a32f8f5a24f199ccbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767576"
---
# <a name="iostxinitsync"></a><span data-ttu-id="e0d3d-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="e0d3d-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="e0d3d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0d3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0d3d-105">Informa o armazenamento de mensagens local que sincronização está prestes a iniciar.</span><span class="sxs-lookup"><span data-stu-id="e0d3d-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="e0d3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0d3d-106">Parameters</span></span>

 <span data-ttu-id="e0d3d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0d3d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e0d3d-108">[in] Sinalizadores para determinar o comportamento apropriado durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="e0d3d-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="e0d3d-109">O Outlook usa esses sinalizadores em cada estado da máquina de estado de replicação para determinar as informações que deverão ser fornecidas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="e0d3d-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="e0d3d-110">Por exemplo, se o cliente passa **SYNC_ONLY_ASSOCIATED**, Outlook retornará somente informações relacionadas a itens associados (ou ocultos).</span><span class="sxs-lookup"><span data-stu-id="e0d3d-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e0d3d-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0d3d-111">See also</span></span>



[<span data-ttu-id="e0d3d-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e0d3d-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="e0d3d-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="e0d3d-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="e0d3d-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="e0d3d-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="e0d3d-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="e0d3d-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="e0d3d-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="e0d3d-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="e0d3d-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="e0d3d-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="e0d3d-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0d3d-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="e0d3d-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e0d3d-119">MAPI Constants</span></span>](mapi-constants.md)


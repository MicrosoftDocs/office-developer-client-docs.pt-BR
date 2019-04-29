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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413350"
---
# <a name="iostxinitsync"></a><span data-ttu-id="f8e67-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="f8e67-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="f8e67-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8e67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8e67-105">Informa o repositório de mensagens local que a sincronização está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="f8e67-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="f8e67-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8e67-106">Parameters</span></span>

 <span data-ttu-id="f8e67-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8e67-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f8e67-108">no Sinalizadores para determinar o comportamento apropriado durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="f8e67-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="f8e67-109">O Outlook usa esses sinalizadores em cada Estado da máquina de estado de replicação para determinar as informações que ele deve fornecer para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f8e67-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="f8e67-110">Por exemplo, se o cliente passar **SYNC_ONLY_ASSOCIATED**, o Outlook retornará apenas informações relacionadas aos itens associados (ou ocultos).</span><span class="sxs-lookup"><span data-stu-id="f8e67-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f8e67-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8e67-111">See also</span></span>



[<span data-ttu-id="f8e67-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f8e67-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="f8e67-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="f8e67-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="f8e67-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="f8e67-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="f8e67-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="f8e67-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="f8e67-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="f8e67-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="f8e67-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="f8e67-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="f8e67-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8e67-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="f8e67-119">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="f8e67-119">MAPI Constants</span></span>](mapi-constants.md)


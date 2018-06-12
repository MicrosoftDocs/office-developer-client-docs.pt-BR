---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767578"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="fd7b5-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="fd7b5-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="fd7b5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fd7b5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fd7b5-105">Define o resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="fd7b5-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="fd7b5-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="fd7b5-106">Parameters</span></span>

 <span data-ttu-id="fd7b5-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="fd7b5-107">_hrSync_</span></span>
  
>  <span data-ttu-id="fd7b5-108">[in] O resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="fd7b5-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fd7b5-109">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="fd7b5-109">Remarks</span></span>

<span data-ttu-id="fd7b5-110">Chame **IOSTX::SetSyncResult** antes de chamar **IOSTX::SyncEnd** para informar o armazenamento local do resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="fd7b5-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd7b5-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd7b5-111">See also</span></span>



[<span data-ttu-id="fd7b5-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fd7b5-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="fd7b5-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="fd7b5-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="fd7b5-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="fd7b5-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="fd7b5-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="fd7b5-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="fd7b5-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="fd7b5-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="fd7b5-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="fd7b5-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="fd7b5-118">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fd7b5-118">MAPI Constants</span></span>](mapi-constants.md)


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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 78ccf72f17ec350d77f2d22d0e6d2fa7c3d97543
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332141"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="b77e2-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b77e2-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="b77e2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b77e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b77e2-105">Define o resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="b77e2-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="b77e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b77e2-106">Parameters</span></span>

 <span data-ttu-id="b77e2-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="b77e2-107">_hrSync_</span></span>
  
>  <span data-ttu-id="b77e2-108">no O resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="b77e2-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b77e2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b77e2-109">Remarks</span></span>

<span data-ttu-id="b77e2-110">Call **IOSTX:: SetSyncResult** antes de chamar **IOSTX:: SyncEnd** para informar o repositório local do resultado da sincronização.</span><span class="sxs-lookup"><span data-stu-id="b77e2-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b77e2-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="b77e2-111">See also</span></span>



[<span data-ttu-id="b77e2-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b77e2-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b77e2-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b77e2-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="b77e2-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b77e2-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b77e2-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b77e2-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="b77e2-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b77e2-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b77e2-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b77e2-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="b77e2-118">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="b77e2-118">MAPI Constants</span></span>](mapi-constants.md)


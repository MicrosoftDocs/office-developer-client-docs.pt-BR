---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767587"
---
# <a name="iostxsyncend"></a><span data-ttu-id="06aef-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="06aef-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="06aef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06aef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06aef-105">Finaliza a sincronização no estado atual e sai desse estado.</span><span class="sxs-lookup"><span data-stu-id="06aef-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="06aef-106">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="06aef-106">Remarks</span></span>

<span data-ttu-id="06aef-107">O cliente deve chamar **IOSTX::SyncEnd** para cada chamada ao [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="06aef-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="06aef-108">A estrutura de dados correspondente contém informações para indicar se o cliente foi concluída com êxito o estado atual para que o Outlook pode limpar o seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="06aef-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06aef-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="06aef-109">See also</span></span>



[<span data-ttu-id="06aef-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="06aef-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="06aef-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="06aef-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="06aef-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="06aef-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="06aef-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="06aef-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="06aef-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="06aef-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="06aef-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="06aef-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="06aef-116">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="06aef-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="06aef-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="06aef-117">MAPI Constants</span></span>](mapi-constants.md)


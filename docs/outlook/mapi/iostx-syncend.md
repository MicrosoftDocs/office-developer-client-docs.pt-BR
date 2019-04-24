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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332148"
---
# <a name="iostxsyncend"></a><span data-ttu-id="5329d-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="5329d-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="5329d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5329d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5329d-105">Termina a sincronização no estado atual e sai desse Estado.</span><span class="sxs-lookup"><span data-stu-id="5329d-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="5329d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5329d-106">Remarks</span></span>

<span data-ttu-id="5329d-107">O cliente deve chamar **IOSTX:: SyncEnd** para cada chamada para [IOSTX:: SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="5329d-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="5329d-108">A estrutura de dados correspondente contém informações para indicar se o cliente concluiu com êxito o estado atual para que o Outlook possa limpar seu estado interno.</span><span class="sxs-lookup"><span data-stu-id="5329d-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5329d-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="5329d-109">See also</span></span>



[<span data-ttu-id="5329d-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="5329d-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="5329d-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="5329d-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="5329d-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="5329d-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="5329d-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="5329d-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="5329d-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="5329d-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="5329d-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="5329d-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="5329d-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5329d-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="5329d-117">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="5329d-117">MAPI Constants</span></span>](mapi-constants.md)


---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Modificado pela última vez: 03 de julho de 2012'
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591328"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="b2a5d-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b2a5d-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="b2a5d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2a5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2a5d-105">Finaliza a sincronização para um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="b2a5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2a5d-106">Parameters</span></span>

 <span data-ttu-id="b2a5d-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="b2a5d-107">_pprog_</span></span>
  
> <span data-ttu-id="b2a5d-108">[in] Interface de **[IMAPIProgress](imapiprogressiunknown.md)** para sincronização de movido ou copiadas de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="b2a5d-109">Consulte mapidefs.h para a definição de tipo de **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2a5d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2a5d-110">Remarks</span></span>

<span data-ttu-id="b2a5d-111">Após a **[IOSTX::SyncBeg](iostx-syncbeg.md)**, armazenamento local entra de [baixar o estado do cabeçalho da mensagem](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="b2a5d-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="b2a5d-112">O cliente baixa um item de mensagem completo (como *pmsgFull* **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="b2a5d-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="b2a5d-113">Se isso for bem-sucedida, o cliente também define *ulFlags* no **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="b2a5d-114">Após **IOSTX::SyncHdrEnd**, o Outlook verifica o resultado em **HDRSYNC** e usa *pprog* e as informações no **HDRSYNC** para atualizar o cabeçalho de mensagem local.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="b2a5d-115">Armazenamento local retorna ao estado em que se encontrava antes do anterior **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2a5d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2a5d-116">See also</span></span>



[<span data-ttu-id="b2a5d-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b2a5d-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b2a5d-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b2a5d-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="b2a5d-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b2a5d-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b2a5d-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b2a5d-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b2a5d-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b2a5d-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="b2a5d-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b2a5d-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b2a5d-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2a5d-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b2a5d-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b2a5d-124">MAPI Constants</span></span>](mapi-constants.md)


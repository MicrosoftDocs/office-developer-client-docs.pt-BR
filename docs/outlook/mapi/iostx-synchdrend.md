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
description: 'Última modificação: 03 de julho de 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332183"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="f28cc-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="f28cc-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="f28cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f28cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f28cc-105">Termina a sincronização de um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f28cc-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="f28cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f28cc-106">Parameters</span></span>

 <span data-ttu-id="f28cc-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="f28cc-107">_pprog_</span></span>
  
> <span data-ttu-id="f28cc-108">no **[Método imapiprogress](imapiprogressiunknown.md)** interface para sincronização de mensagens movidas ou copiadas.</span><span class="sxs-lookup"><span data-stu-id="f28cc-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="f28cc-109">Consulte mapidefs. h para a definição de tipo de **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="f28cc-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f28cc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f28cc-110">Remarks</span></span>

<span data-ttu-id="f28cc-111">Após o **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, o repositório local entra no [status do cabeçalho da mensagem de download](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="f28cc-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="f28cc-112">O cliente baixa um item de mensagem completo (como *pmsgFull* no **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="f28cc-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="f28cc-113">Se isso for bem-sucedido, o cliente também definirá *parâmetroulflags* no **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="f28cc-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="f28cc-114">Após o **IOSTX:: SyncHdrEnd**, o Outlook verifica o resultado em **HDRSYNC** e usa *Pprog* e as informações em **HDRSYNC** para atualizar o cabeçalho da mensagem local.</span><span class="sxs-lookup"><span data-stu-id="f28cc-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="f28cc-115">O repositório local retorna ao estado em que estava antes da IOSTX anterior **[:: SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="f28cc-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f28cc-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f28cc-116">See also</span></span>



[<span data-ttu-id="f28cc-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="f28cc-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="f28cc-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="f28cc-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="f28cc-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="f28cc-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="f28cc-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="f28cc-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="f28cc-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="f28cc-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="f28cc-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="f28cc-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="f28cc-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f28cc-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="f28cc-124">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="f28cc-124">MAPI Constants</span></span>](mapi-constants.md)


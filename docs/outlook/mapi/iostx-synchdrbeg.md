---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317154"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="a7f2c-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="a7f2c-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="a7f2c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7f2c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7f2c-105">Inicia a sincronização de um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="a7f2c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f2c-106">Parameters</span></span>

 <span data-ttu-id="a7f2c-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="a7f2c-107">_cbeid_</span></span>
  
> <span data-ttu-id="a7f2c-108">no O número de bytes na ID de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="a7f2c-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="a7f2c-109">_lpeid_</span></span>
  
> <span data-ttu-id="a7f2c-110">no A identificação de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="a7f2c-111">_PPV_</span><span class="sxs-lookup"><span data-stu-id="a7f2c-111">_ppv_</span></span>
  
>  <span data-ttu-id="a7f2c-112">[in]/[out] ponteiro para a estrutura **[HDRSYNC](hdrsync.md)** do cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a7f2c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7f2c-113">Remarks</span></span>

<span data-ttu-id="a7f2c-114">Após o **IOSTX:: SyncHdrBeg**, o repositório local transita para o [estado de cabeçalho da mensagem de download](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="a7f2c-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="a7f2c-115">O Outlook é inicializado para o cliente a estrutura **HDRSYNC** com a representação atual do cabeçalho da mensagem no repositório e na pasta pai.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="a7f2c-116">O cliente deve baixar um item de mensagem completo (como *pmsgFull* no **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="a7f2c-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="a7f2c-117">Se isso tiver sido bem-sucedido, o cliente também define *parâmetroulflags* no **HDRSYNC** como **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="a7f2c-118">Após o **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o cabeçalho da mensagem local.</span><span class="sxs-lookup"><span data-stu-id="a7f2c-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7f2c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7f2c-119">See also</span></span>



[<span data-ttu-id="a7f2c-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a7f2c-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="a7f2c-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="a7f2c-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="a7f2c-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="a7f2c-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="a7f2c-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="a7f2c-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="a7f2c-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="a7f2c-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="a7f2c-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="a7f2c-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="a7f2c-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7f2c-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="a7f2c-127">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="a7f2c-127">MAPI Constants</span></span>](mapi-constants.md)


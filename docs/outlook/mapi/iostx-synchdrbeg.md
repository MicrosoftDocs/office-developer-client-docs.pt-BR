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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767580"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="d2b00-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="d2b00-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="d2b00-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d2b00-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d2b00-105">Inicia a sincronização de um cabeçalho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2b00-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="d2b00-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2b00-106">Parameters</span></span>

 <span data-ttu-id="d2b00-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="d2b00-107">_cbeid_</span></span>
  
> <span data-ttu-id="d2b00-108">[in] O número de bytes na identificação de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2b00-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="d2b00-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="d2b00-109">_lpeid_</span></span>
  
> <span data-ttu-id="d2b00-110">[in] A identificação de entrada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2b00-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="d2b00-111">_ppv_</span><span class="sxs-lookup"><span data-stu-id="d2b00-111">_ppv_</span></span>
  
>  <span data-ttu-id="d2b00-112">[in] / [out] ponteiro para a estrutura **[HDRSYNC](hdrsync.md)** para o cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2b00-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d2b00-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2b00-113">Remarks</span></span>

<span data-ttu-id="d2b00-114">Após a **IOSTX::SyncHdrBeg**, o local armazenar transições a [baixar o estado do cabeçalho da mensagem](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="d2b00-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="d2b00-115">Inicializa o Outlook para o cliente a estrutura **HDRSYNC** com a representação atual do cabeçalho da mensagem no repositório e a pasta pai.</span><span class="sxs-lookup"><span data-stu-id="d2b00-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="d2b00-116">O cliente, em seguida, deve baixar um item de mensagem completo (como *pmsgFull* **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="d2b00-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="d2b00-117">Se isso foi bem-sucedida, o cliente também definirá *ulFlags* em **HDRSYNC** **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="d2b00-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="d2b00-118">Após a **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, o Outlook verifica o resultado em **HDRSYNC** e usa as informações em **HDRSYNC** para atualizar o cabeçalho de mensagem local.</span><span class="sxs-lookup"><span data-stu-id="d2b00-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2b00-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2b00-119">See also</span></span>



[<span data-ttu-id="d2b00-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d2b00-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="d2b00-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="d2b00-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="d2b00-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="d2b00-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="d2b00-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="d2b00-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="d2b00-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="d2b00-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="d2b00-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="d2b00-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="d2b00-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2b00-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="d2b00-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d2b00-127">MAPI Constants</span></span>](mapi-constants.md)


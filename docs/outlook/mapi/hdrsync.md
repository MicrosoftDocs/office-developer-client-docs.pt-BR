---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 261a59e628320f384deeb760ba71c9c0386cfde6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576040"
---
# <a name="hdrsync"></a><span data-ttu-id="d3f32-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="d3f32-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="d3f32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3f32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3f32-105">Informações para sincronizar o cabeçalho da mensagem durante a [baixar o estado do cabeçalho da mensagem](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="d3f32-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d3f32-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d3f32-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="d3f32-107">Members</span><span class="sxs-lookup"><span data-stu-id="d3f32-107">Members</span></span>

 <span data-ttu-id="d3f32-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="d3f32-108">_pupmsg_</span></span>
  
- <span data-ttu-id="d3f32-109">[out] Informações de cabeçalho da mensagem atual no armazenamento local.</span><span class="sxs-lookup"><span data-stu-id="d3f32-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="d3f32-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="d3f32-110">_feidPar_</span></span>
  
- <span data-ttu-id="d3f32-111">[out] Identificação de entrada para a pasta pai do item de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d3f32-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="d3f32-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="d3f32-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="d3f32-113">[uto] Esse membro é reservado para uso interno do Outlook e não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d3f32-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d3f32-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3f32-114">_ulFlags_</span></span>
  
- <span data-ttu-id="d3f32-115">[in] Sinalizadores para modificar o comportamento:</span><span class="sxs-lookup"><span data-stu-id="d3f32-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="d3f32-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="d3f32-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="d3f32-117">[in] Item completo reside no mesmo armazenamento local como o item de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d3f32-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="d3f32-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="d3f32-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="d3f32-119">[in] Otimize as operações de cópia interna.</span><span class="sxs-lookup"><span data-stu-id="d3f32-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="d3f32-120">Isso pode causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="d3f32-120">This might cause data loss.</span></span> <span data-ttu-id="d3f32-121">**HSF_LOCAL** deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="d3f32-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="d3f32-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="d3f32-122">HSF_OK</span></span>
    
  - <span data-ttu-id="d3f32-123">[in] Sincronização de cabeçalho foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d3f32-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="d3f32-124">O cliente define isso depois de baixar informações do servidor.</span><span class="sxs-lookup"><span data-stu-id="d3f32-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="d3f32-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="d3f32-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="d3f32-126">[in] O item de mensagem completo, incluindo o cabeçalho da mensagem é baixado do servidor.</span><span class="sxs-lookup"><span data-stu-id="d3f32-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="d3f32-127">Consulte mapidefs.h para a definição de tipo de **LPMESSAGE**.</span><span class="sxs-lookup"><span data-stu-id="d3f32-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d3f32-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3f32-128">See also</span></span>



[<span data-ttu-id="d3f32-129">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d3f32-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d3f32-130">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d3f32-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d3f32-131">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="d3f32-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d3f32-132">FEID</span><span class="sxs-lookup"><span data-stu-id="d3f32-132">FEID</span></span>](feid.md)


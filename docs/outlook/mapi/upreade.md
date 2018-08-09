---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770688"
---
# <a name="upreade"></a><span data-ttu-id="6adcb-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="6adcb-103">UPREADE</span></span>

<span data-ttu-id="6adcb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6adcb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6adcb-105">Informações estendidas para carregar o estado de leitura de um item durante o [carregamento ler o estado de status](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="6adcb-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6adcb-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6adcb-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="6adcb-107">Members</span><span class="sxs-lookup"><span data-stu-id="6adcb-107">Members</span></span>

<span data-ttu-id="6adcb-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6adcb-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="6adcb-109">[out] / [in] sinalizadores para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="6adcb-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="6adcb-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="6adcb-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="6adcb-111">[out] Item é oculto.</span><span class="sxs-lookup"><span data-stu-id="6adcb-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="6adcb-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="6adcb-112">UPR_READ</span></span>
    
    - <span data-ttu-id="6adcb-113">[out] O status de leitura do item foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6adcb-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="6adcb-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="6adcb-114">UPR_OK</span></span>
    
    - <span data-ttu-id="6adcb-115">[in] Carregamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6adcb-115">[in] Upload was successful.</span></span> <span data-ttu-id="6adcb-116">O cliente define esta após carregar as informações para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6adcb-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="6adcb-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="6adcb-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="6adcb-118">[in] Carrega o status de leitura do item agora, em vez de aguardar até o final da [carregar o estado de tabela](upload-table-state.md) para processamento em lotes mais de um item.</span><span class="sxs-lookup"><span data-stu-id="6adcb-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="6adcb-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="6adcb-119">_skey_</span></span>
  
> <span data-ttu-id="6adcb-120">[out] Chave de origem do item.</span><span class="sxs-lookup"><span data-stu-id="6adcb-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6adcb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6adcb-121">See also</span></span>

- [<span data-ttu-id="6adcb-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="6adcb-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="6adcb-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="6adcb-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="6adcb-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6adcb-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="6adcb-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="6adcb-125">UPREAD</span></span>](upread.md)

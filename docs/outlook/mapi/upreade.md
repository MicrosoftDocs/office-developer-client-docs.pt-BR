---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338861"
---
# <a name="upreade"></a><span data-ttu-id="53ba4-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="53ba4-103">UPREADE</span></span>

<span data-ttu-id="53ba4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ba4-105">Informações estendidas para carregar o estado de leitura de um item durante o [estado carregar status de leitura](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="53ba4-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="53ba4-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="53ba4-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="53ba4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="53ba4-107">Members</span></span>

<span data-ttu-id="53ba4-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53ba4-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="53ba4-109">[out]/[in] flags para determinar o comportamento apropriado durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="53ba4-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="53ba4-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="53ba4-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="53ba4-111">bota O item está oculto.</span><span class="sxs-lookup"><span data-stu-id="53ba4-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="53ba4-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="53ba4-112">UPR_READ</span></span>
    
    - <span data-ttu-id="53ba4-113">bota O status de leitura do item foi alterado.</span><span class="sxs-lookup"><span data-stu-id="53ba4-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="53ba4-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="53ba4-114">UPR_OK</span></span>
    
    - <span data-ttu-id="53ba4-115">no O upload foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="53ba4-115">[in] Upload was successful.</span></span> <span data-ttu-id="53ba4-116">O cliente define isso após carregar informações no servidor.</span><span class="sxs-lookup"><span data-stu-id="53ba4-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="53ba4-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="53ba4-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="53ba4-118">no Carregar o status de leitura do item agora, em vez de esperar para o final do [estado de carregamento da tabela](upload-table-state.md) para processar mais de um item.</span><span class="sxs-lookup"><span data-stu-id="53ba4-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="53ba4-119">_skey_</span><span class="sxs-lookup"><span data-stu-id="53ba4-119">_skey_</span></span>
  
> <span data-ttu-id="53ba4-120">bota Chave de origem do item.</span><span class="sxs-lookup"><span data-stu-id="53ba4-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53ba4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="53ba4-121">See also</span></span>

- [<span data-ttu-id="53ba4-122">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="53ba4-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="53ba4-123">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="53ba4-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="53ba4-124">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="53ba4-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="53ba4-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="53ba4-125">UPREAD</span></span>](upread.md)


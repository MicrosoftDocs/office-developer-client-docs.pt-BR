---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581122"
---
# <a name="updel"></a><span data-ttu-id="b4614-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="b4614-103">UPDEL</span></span>

  
  
<span data-ttu-id="b4614-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4614-105">Informações para itens que foram excluídos em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="b4614-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="b4614-106">Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="b4614-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b4614-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b4614-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b4614-108">Members</span><span class="sxs-lookup"><span data-stu-id="b4614-108">Members</span></span>

 <span data-ttu-id="b4614-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="b4614-109">_pupde_</span></span>
  
>  <span data-ttu-id="b4614-110">[out] Vetor de [UPDELE](updele.md) entradas.</span><span class="sxs-lookup"><span data-stu-id="b4614-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="b4614-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="b4614-111">_cEnt_</span></span>
  
> <span data-ttu-id="b4614-112">[out] Número de entradas em *pupde* .</span><span class="sxs-lookup"><span data-stu-id="b4614-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b4614-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4614-113">See also</span></span>



[<span data-ttu-id="b4614-114">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="b4614-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b4614-115">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="b4614-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b4614-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4614-116">MAPI Constants</span></span>](mapi-constants.md)


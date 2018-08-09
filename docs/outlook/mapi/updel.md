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
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770663"
---
# <a name="updel"></a><span data-ttu-id="f6569-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="f6569-103">UPDEL</span></span>

  
  
<span data-ttu-id="f6569-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6569-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6569-105">Informações para itens que foram excluídos em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="f6569-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="f6569-106">Essas informações são usadas durante o [carregamento excluir o estado de status](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="f6569-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f6569-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f6569-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="f6569-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6569-108">Members</span></span>

 <span data-ttu-id="f6569-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="f6569-109">_pupde_</span></span>
  
>  <span data-ttu-id="f6569-110">[out] Vetor de [UPDELE](updele.md) entradas.</span><span class="sxs-lookup"><span data-stu-id="f6569-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="f6569-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="f6569-111">_cEnt_</span></span>
  
> <span data-ttu-id="f6569-112">[out] Número de entradas em *pupde* .</span><span class="sxs-lookup"><span data-stu-id="f6569-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f6569-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6569-113">See also</span></span>



[<span data-ttu-id="f6569-114">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="f6569-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f6569-115">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="f6569-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f6569-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f6569-116">MAPI Constants</span></span>](mapi-constants.md)


---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fa3c0b90a64c90a7c854cb22ac75438fa5fca23f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770680"
---
# <a name="upread"></a><span data-ttu-id="d858f-103">UPREAD</span><span class="sxs-lookup"><span data-stu-id="d858f-103">UPREAD</span></span>

  
  
<span data-ttu-id="d858f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d858f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d858f-105">Informações para carregar o estado de leitura dos itens durante o [carregamento ler o estado de status](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="d858f-105">Information for uploading the read state of items during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d858f-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d858f-106">Quick info</span></span>

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="d858f-107">Members</span><span class="sxs-lookup"><span data-stu-id="d858f-107">Members</span></span>

 <span data-ttu-id="d858f-108">_pupre_</span><span class="sxs-lookup"><span data-stu-id="d858f-108">_pupre_</span></span>
  
>  <span data-ttu-id="d858f-109">[out] Vetor de **[UPREADE](upreade.md)** entradas.</span><span class="sxs-lookup"><span data-stu-id="d858f-109">[out] Vector of **[UPREADE](upreade.md)** entries.</span></span> 
    
 <span data-ttu-id="d858f-110">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="d858f-110">_cEnt_</span></span>
  
>  <span data-ttu-id="d858f-111">[out] Número de entradas **UPREADE** .</span><span class="sxs-lookup"><span data-stu-id="d858f-111">[out] Number of **UPREADE** entries.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d858f-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="d858f-112">See also</span></span>



[<span data-ttu-id="d858f-113">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="d858f-113">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d858f-114">Sobre a máquina de estado de replicação</span><span class="sxs-lookup"><span data-stu-id="d858f-114">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d858f-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d858f-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d858f-116">UPREADE</span><span class="sxs-lookup"><span data-stu-id="d858f-116">UPREADE</span></span>](upreade.md)


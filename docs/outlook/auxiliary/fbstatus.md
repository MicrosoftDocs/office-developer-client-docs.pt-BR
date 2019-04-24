---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Uma enumeração para o status de disponibilidade dos blocos de disponibilidade.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319723"
---
# <a name="fbstatus"></a><span data-ttu-id="22b3e-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="22b3e-103">FBStatus</span></span>

<span data-ttu-id="22b3e-104">Uma enumeração para o status de disponibilidade dos blocos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="22b3e-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="22b3e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="22b3e-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="22b3e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="22b3e-106">Remarks</span></span>

<span data-ttu-id="22b3e-107">O status de disponibilidade de um bloco de tempo determina como ele é exibido em um calendário: **livre**, **ocupado**, **provisório**ou **ausência temporária**.</span><span class="sxs-lookup"><span data-stu-id="22b3e-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22b3e-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="22b3e-108">See also</span></span>

- [<span data-ttu-id="22b3e-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="22b3e-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="22b3e-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="22b3e-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)


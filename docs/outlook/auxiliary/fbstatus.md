---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Uma enumeração para o status livre/ocupado de blocos de livre/ocupado.
ms.openlocfilehash: 67d710f82856dc8ff4839c926018eef88d355f73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19765808"
---
# <a name="fbstatus"></a><span data-ttu-id="c2a3c-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="c2a3c-103">FBStatus</span></span>

<span data-ttu-id="c2a3c-104">Uma enumeração para o status livre/ocupado de blocos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c2a3c-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c2a3c-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="c2a3c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2a3c-106">Remarks</span></span>

<span data-ttu-id="c2a3c-107">O status livre/ocupado de um bloco de tempo determina como ele é exibido em um calendário: **disponível**, **ocupado**, **Provisório**ou **Ausência temporária**.</span><span class="sxs-lookup"><span data-stu-id="c2a3c-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2a3c-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2a3c-108">See also</span></span>

- [<span data-ttu-id="c2a3c-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="c2a3c-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="c2a3c-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="c2a3c-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)


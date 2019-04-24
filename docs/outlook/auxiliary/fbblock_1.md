---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define um bloco de dados de disponibilidade. Este é um item em um calendário representado por um compromisso ou uma solicitação de reunião.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317665"
---
# <a name="fbblock1"></a><span data-ttu-id="69ac0-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="69ac0-104">FBBlock_1</span></span>

<span data-ttu-id="69ac0-105">Define um bloco de dados de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="69ac0-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="69ac0-106">Este é um item em um calendário representado por um compromisso ou uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="69ac0-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="69ac0-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="69ac0-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="69ac0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="69ac0-108">Members</span></span>

<span data-ttu-id="69ac0-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="69ac0-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="69ac0-110">A hora de início para o bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="69ac0-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="69ac0-111">Para obter mais informações, consulte [usar tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="69ac0-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="69ac0-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="69ac0-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="69ac0-113">A hora de término do bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="69ac0-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="69ac0-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="69ac0-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="69ac0-115">O status de disponibilidade desse bloco, indicando se o usuário está fora do escritório, ocupado, provisório ou livre, durante o período de tempo entre _m_tmStart_ e _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="69ac0-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69ac0-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ac0-116">See also</span></span>

- [<span data-ttu-id="69ac0-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="69ac0-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="69ac0-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="69ac0-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="69ac0-119">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="69ac0-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


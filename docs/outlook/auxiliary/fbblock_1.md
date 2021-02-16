---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define um bloco de dados de livre/ocupado. Este é um item em um calendário representado por um compromisso ou solicitação de reunião.
ms.openlocfilehash: 60d2ff50081a8950a397df6f2f6bbfd37d3bdb61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413196"
---
# <a name="fbblock_1"></a><span data-ttu-id="4f23b-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="4f23b-104">FBBlock_1</span></span>

<span data-ttu-id="4f23b-105">Define um bloco de dados de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="4f23b-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="4f23b-106">Este é um item em um calendário representado por um compromisso ou uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="4f23b-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4f23b-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4f23b-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="4f23b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4f23b-108">Members</span></span>

<span data-ttu-id="4f23b-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="4f23b-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="4f23b-110">A hora de início do bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="4f23b-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="4f23b-111">Para obter mais informações, [consulte Usar o tempo relativo para acessar dados de livre/ocupado.](how-to-use-relative-time-to-access-free-busy-data.md)</span><span class="sxs-lookup"><span data-stu-id="4f23b-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="4f23b-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="4f23b-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="4f23b-113">A hora de término do bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="4f23b-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="4f23b-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="4f23b-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="4f23b-115">O status de livre/ocupado para esse bloco, indicando se o usuário está fora do escritório,  ocupado, provisório ou livre, durante o período de tempo entre m_tmStart e _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="4f23b-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f23b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f23b-116">See also</span></span>

- [<span data-ttu-id="4f23b-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="4f23b-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="4f23b-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="4f23b-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="4f23b-119">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="4f23b-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413196"
---
# <a name="fbblock1"></a><span data-ttu-id="65dc2-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="65dc2-104">FBBlock_1</span></span>

<span data-ttu-id="65dc2-105">Define um bloco de dados de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="65dc2-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="65dc2-106">Este é um item em um calendário representado por um compromisso ou uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="65dc2-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="65dc2-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="65dc2-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="65dc2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="65dc2-108">Members</span></span>

<span data-ttu-id="65dc2-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="65dc2-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="65dc2-110">A hora de início para o bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="65dc2-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="65dc2-111">Para obter mais informações, consulte [usar tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="65dc2-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="65dc2-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="65dc2-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="65dc2-113">A hora de término do bloco, expressa em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="65dc2-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="65dc2-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="65dc2-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="65dc2-115">O status de disponibilidade desse bloco, indicando se o usuário está fora do escritório, ocupado, provisório ou livre, durante o período de tempo entre _m_tmStart_ e _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="65dc2-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="65dc2-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="65dc2-116">See also</span></span>

- [<span data-ttu-id="65dc2-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="65dc2-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="65dc2-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="65dc2-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="65dc2-119">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="65dc2-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


---
title: FBBlock_1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: da67171d-d25f-3424-1409-33189ac63a12
description: Define um bloco de informações de disponibilidade de dados. Este é um item em um calendário representado por uma solicitação de reunião ou compromisso.
ms.openlocfilehash: 93418e3777e9d9f0a016822ea5897b8fccc37ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765797"
---
# <a name="fbblock1"></a><span data-ttu-id="cfe7b-104">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="cfe7b-104">FBBlock_1</span></span>

<span data-ttu-id="cfe7b-105">Define um bloco de informações de disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="cfe7b-105">Defines a free/busy block of data.</span></span> <span data-ttu-id="cfe7b-106">Este é um item em um calendário representado por uma solicitação de reunião ou compromisso.</span><span class="sxs-lookup"><span data-stu-id="cfe7b-106">This is an item on a calendar represented by an appointment or meeting request.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cfe7b-107">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="cfe7b-107">Quick info</span></span>

```cpp
typedef struct  tagFBBlock_1 
    { 
    long m_tmStart; 
    long m_tmEnd; 
    FBStatus m_fbstatus; 
    }FBBlock_1; 

```

## <a name="members"></a><span data-ttu-id="cfe7b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cfe7b-108">Members</span></span>

<span data-ttu-id="cfe7b-109">_m_tmStart_</span><span class="sxs-lookup"><span data-stu-id="cfe7b-109">_m_tmStart_</span></span>
  
> <span data-ttu-id="cfe7b-110">A hora de início para o bloco, expresso em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="cfe7b-110">The start time for the block, expressed in relative time.</span></span> <span data-ttu-id="cfe7b-111">Para obter mais informações, consulte [tempo relativo para acessar informações de disponibilidade de dados de uso](how-to-use-relative-time-to-access-free-busy-data.md).</span><span class="sxs-lookup"><span data-stu-id="cfe7b-111">For more information, see [Use relative time to access free/busy data](how-to-use-relative-time-to-access-free-busy-data.md).</span></span>
    
<span data-ttu-id="cfe7b-112">_m_tmEnd_</span><span class="sxs-lookup"><span data-stu-id="cfe7b-112">_m_tmEnd_</span></span>
  
> <span data-ttu-id="cfe7b-113">A hora de término para o bloco, expresso em tempo relativo.</span><span class="sxs-lookup"><span data-stu-id="cfe7b-113">The end time for the block, expressed in relative time.</span></span>
    
<span data-ttu-id="cfe7b-114">_m_fbStatus_</span><span class="sxs-lookup"><span data-stu-id="cfe7b-114">_m_fbStatus_</span></span>
  
> <span data-ttu-id="cfe7b-115">O status livre/ocupado para este bloco, que indica se o usuário está fora do escritório, ocupado, provisório ou livre, durante o período de tempo entre _m_tmStart_ e _m_tmEnd_.</span><span class="sxs-lookup"><span data-stu-id="cfe7b-115">The free/busy status for this block, indicating whether the user is out-of-office, busy, tentative, or free, during the time period between  _m_tmStart_ and  _m_tmEnd_.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cfe7b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfe7b-116">See also</span></span>

- [<span data-ttu-id="cfe7b-117">FBStatus</span><span class="sxs-lookup"><span data-stu-id="cfe7b-117">FBStatus</span></span>](fbstatus.md)
- [<span data-ttu-id="cfe7b-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="cfe7b-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)
- [<span data-ttu-id="cfe7b-119">Use o tempo relativo para acessar dados do tipo disponível/ocupado</span><span class="sxs-lookup"><span data-stu-id="cfe7b-119">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


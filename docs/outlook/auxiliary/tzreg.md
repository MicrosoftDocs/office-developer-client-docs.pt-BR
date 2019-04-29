---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Define quando o horário de verão começa, quando ocorre o retorno do horário padrão e quantas horas o turno de horário de verão é.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419363"
---
# <a name="tzreg"></a><span data-ttu-id="7ec86-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="7ec86-103">TZREG</span></span>

<span data-ttu-id="7ec86-104">Define quando o horário de verão começa, quando ocorre o retorno do horário padrão e quantas horas o turno de horário de verão é.</span><span class="sxs-lookup"><span data-stu-id="7ec86-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7ec86-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7ec86-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="7ec86-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7ec86-106">Members</span></span>

<span data-ttu-id="7ec86-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="7ec86-107">_lBias_</span></span>
  
> <span data-ttu-id="7ec86-108">O deslocamento do horário de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="7ec86-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="7ec86-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="7ec86-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="7ec86-110">O deslocamento de diferença durante o horário padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec86-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="7ec86-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="7ec86-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="7ec86-112">O deslocamento de diferença durante o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="7ec86-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="7ec86-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="7ec86-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="7ec86-114">O tempo para mudar para o horário padrão.</span><span class="sxs-lookup"><span data-stu-id="7ec86-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="7ec86-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="7ec86-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="7ec86-116">O tempo para mudar para o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="7ec86-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ec86-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec86-117">Remarks</span></span>

<span data-ttu-id="7ec86-118">Essa estrutura é semelhante a **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="7ec86-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="7ec86-119">Esta é a estrutura usada por clientes herdados para armazenar informações de fuso horário para reuniões recorrentes.</span><span class="sxs-lookup"><span data-stu-id="7ec86-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ec86-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec86-120">See also</span></span>

- [<span data-ttu-id="7ec86-121">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="7ec86-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="7ec86-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="7ec86-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="7ec86-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="7ec86-123">TZRULE</span></span>](tzrule.md)


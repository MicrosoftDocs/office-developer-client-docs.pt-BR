---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica as informações de uma regra de fuso horário sobre quando inicia o horário de verão e o ano em que essa regra de fuso horário primeiro entrará em vigor.
ms.openlocfilehash: 77d56d238d959992bfadd2d8c143391ca6fa4d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766084"
---
# <a name="tzrule"></a><span data-ttu-id="be4cc-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="be4cc-103">TZRULE</span></span>

<span data-ttu-id="be4cc-104">Especifica as informações de uma regra de fuso horário sobre quando inicia o horário de verão e o ano em que essa regra de fuso horário primeiro entrará em vigor.</span><span class="sxs-lookup"><span data-stu-id="be4cc-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="be4cc-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="be4cc-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="be4cc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="be4cc-106">Members</span></span>

<span data-ttu-id="be4cc-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="be4cc-107">_wFlags_</span></span>
  
> <span data-ttu-id="be4cc-108">Os sinalizadores definidos para este membro identificam detalhes específicos para essa regra de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="be4cc-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="be4cc-109">Os sinalizadores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="be4cc-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="be4cc-110">**TZRULE_FLAG_EFFECTIVE_TZREG** — identifica a regra como aquele que deve ser usada no momento.</span><span class="sxs-lookup"><span data-stu-id="be4cc-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="be4cc-111">Somente uma regra pode ser marcada como a regra efetiva.</span><span class="sxs-lookup"><span data-stu-id="be4cc-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="be4cc-112">Todas as outras regras são apenas para fins de comparação.</span><span class="sxs-lookup"><span data-stu-id="be4cc-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="be4cc-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** — em reuniões recorrentes, identifica a regra como correspondência da regra na [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="be4cc-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](http://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="be4cc-114">Isso pode ser usado para detectar se **PidLidTimeZoneStruct** tiver sido modificada significativamente por um cliente herdado, qual seria caso contrário, não sabem da propriedade nova e mais completa.</span><span class="sxs-lookup"><span data-stu-id="be4cc-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="be4cc-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="be4cc-115">_stStart_</span></span>
  
> <span data-ttu-id="be4cc-116">A hora no tempo Universal Coordenado (UTC) que a regra de fuso horário é iniciada.</span><span class="sxs-lookup"><span data-stu-id="be4cc-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="be4cc-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="be4cc-117">_TZReg_</span></span>
  
> <span data-ttu-id="be4cc-118">As informações de fuso horário para a regra de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="be4cc-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be4cc-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="be4cc-119">Remarks</span></span>

<span data-ttu-id="be4cc-120">Essa estrutura aumenta [TZREG](tzreg.md) fornecendo informações adicionais indicando quando as regras de fuso horário entrem em vigor.</span><span class="sxs-lookup"><span data-stu-id="be4cc-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be4cc-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="be4cc-121">See also</span></span>

- [<span data-ttu-id="be4cc-122">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="be4cc-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="be4cc-123">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="be4cc-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="be4cc-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="be4cc-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="be4cc-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="be4cc-125">TZDEFINITION</span></span>](tzdefinition.md)


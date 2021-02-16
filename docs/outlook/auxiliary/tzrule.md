---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Especifica as informações de uma regra de fuso horário sobre quando começa o horário de verão e o ano em que essa regra de fuso horário entrou em vigor.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328613"
---
# <a name="tzrule"></a><span data-ttu-id="203dd-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="203dd-103">TZRULE</span></span>

<span data-ttu-id="203dd-104">Especifica as informações de uma regra de fuso horário sobre quando começa o horário de verão e o ano em que essa regra de fuso horário entrou em vigor.</span><span class="sxs-lookup"><span data-stu-id="203dd-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="203dd-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="203dd-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="203dd-106">Members</span><span class="sxs-lookup"><span data-stu-id="203dd-106">Members</span></span>

<span data-ttu-id="203dd-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="203dd-107">_wFlags_</span></span>
  
> <span data-ttu-id="203dd-108">Os sinalizadores definidos para esse membro identificam os detalhes específicos da regra de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="203dd-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="203dd-109">Os sinalizadores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="203dd-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="203dd-110">**TZRULE_FLAG_EFFECTIVE_TZREG**: identifica a regra que deve ser usada no momento.</span><span class="sxs-lookup"><span data-stu-id="203dd-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="203dd-111">Somente uma regra pode ser marcada como a regra efetiva.</span><span class="sxs-lookup"><span data-stu-id="203dd-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="203dd-112">Todas as regras são apenas para fins de comparação.</span><span class="sxs-lookup"><span data-stu-id="203dd-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="203dd-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG**: em reuniões recorrentes, identifica a regra como correspondente à regra em [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="203dd-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="203dd-114">Pode ser usado para detectar se **PidLidTimeZoneStruct** foi modificado significativamente por um cliente herdado, o que, caso contrário, passaria despercebido pelo nova propriedade mais completa.</span><span class="sxs-lookup"><span data-stu-id="203dd-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="203dd-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="203dd-115">_stStart_</span></span>
  
> <span data-ttu-id="203dd-116">A hora em UTC (Tempo Universal Coordenado) que a regra de fuso horário iniciou.</span><span class="sxs-lookup"><span data-stu-id="203dd-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="203dd-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="203dd-117">_TZReg_</span></span>
  
> <span data-ttu-id="203dd-118">As informações de fuso horário para a regra de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="203dd-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="203dd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="203dd-119">Remarks</span></span>

<span data-ttu-id="203dd-120">Essa estrutura aumenta [TZREG](tzreg.md) fornecendo informações adicionais que indicam quando as regras de fuso horário entram em vigor.</span><span class="sxs-lookup"><span data-stu-id="203dd-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="203dd-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="203dd-121">See also</span></span>

- [<span data-ttu-id="203dd-122">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="203dd-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="203dd-123">Constantes (APIs exportadas pelo Outlook)</span><span class="sxs-lookup"><span data-stu-id="203dd-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="203dd-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="203dd-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="203dd-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="203dd-125">TZDEFINITION</span></span>](tzdefinition.md)


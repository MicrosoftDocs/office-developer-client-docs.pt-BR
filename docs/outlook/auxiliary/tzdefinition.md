---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa um fuso horário inteiro, incluindo todas as regras de turno de fuso horário histórico, atual e futuro para o horário de verão.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429338"
---
# <a name="tzdefinition"></a><span data-ttu-id="48ed4-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="48ed4-103">TZDEFINITION</span></span>

<span data-ttu-id="48ed4-104">Representa um fuso horário inteiro, incluindo todas as regras de turno de fuso horário histórico, atual e futuro para o horário de verão.</span><span class="sxs-lookup"><span data-stu-id="48ed4-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="48ed4-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="48ed4-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="48ed4-106">Members</span><span class="sxs-lookup"><span data-stu-id="48ed4-106">Members</span></span>

<span data-ttu-id="48ed4-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="48ed4-107">_wFlags_</span></span>
  
> <span data-ttu-id="48ed4-108">Indica que o nome da chave que representa o fuso horário no Registro do Windows é válido.</span><span class="sxs-lookup"><span data-stu-id="48ed4-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="48ed4-109">Como cada fuso horário deve ser sempre identificado por um nome de chave, esse membro sempre deve ter o valor **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="48ed4-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="48ed4-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="48ed4-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="48ed4-111">O nome da chave para este fuso horário no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="48ed4-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="48ed4-112">Esse nome não deve ser localizado.</span><span class="sxs-lookup"><span data-stu-id="48ed4-112">This name must not be localized.</span></span> <span data-ttu-id="48ed4-113">Ele tem um tamanho máximo de **MAX_PATH**, que é definido no arquivo de header windows.h do Software Development Kit do Windows (SDK do Windows).</span><span class="sxs-lookup"><span data-stu-id="48ed4-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="48ed4-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="48ed4-114">_cRules_</span></span>
  
> <span data-ttu-id="48ed4-115">O número de regras de fuso horário para esta definição.</span><span class="sxs-lookup"><span data-stu-id="48ed4-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="48ed4-116">O número máximo de regras é **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="48ed4-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="48ed4-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="48ed4-117">_rgRules_</span></span>
  
> <span data-ttu-id="48ed4-118">Uma matriz de regras que descrevem quando ocorrem turnos.</span><span class="sxs-lookup"><span data-stu-id="48ed4-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48ed4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="48ed4-119">Remarks</span></span>

<span data-ttu-id="48ed4-120">Deve haver pelo menos uma regra em  *rgRules*  .</span><span class="sxs-lookup"><span data-stu-id="48ed4-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="48ed4-121">A primeira regra em  *rgRules*  é considerada a regra a ser usada até que a segunda regra seja iniciada, independentemente do  *stStart*  na primeira regra.</span><span class="sxs-lookup"><span data-stu-id="48ed4-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="48ed4-122">As regras devem ser ordenadas da mais antiga para a mais recente.</span><span class="sxs-lookup"><span data-stu-id="48ed4-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="48ed4-123">Não há sobreposição permitida entre as regras, portanto, uma regra anterior é considerada para terminar quando uma nova regra é iniciada.</span><span class="sxs-lookup"><span data-stu-id="48ed4-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="48ed4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="48ed4-124">See also</span></span>

- [<span data-ttu-id="48ed4-125">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="48ed4-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="48ed4-126">Sobre a alteração programática da base de calendários para o horário de verão</span><span class="sxs-lookup"><span data-stu-id="48ed4-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="48ed4-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="48ed4-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)


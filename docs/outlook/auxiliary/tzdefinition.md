---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Representa um fuso horário inteiro, incluindo todas as regras de shift históricas, atuais e futuros de fuso horário de verão.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766096"
---
# <a name="tzdefinition"></a><span data-ttu-id="b0876-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b0876-103">TZDEFINITION</span></span>

<span data-ttu-id="b0876-104">Representa um fuso horário inteiro, incluindo todas as regras de shift históricas, atuais e futuros de fuso horário de verão.</span><span class="sxs-lookup"><span data-stu-id="b0876-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b0876-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b0876-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="b0876-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b0876-106">Members</span></span>

<span data-ttu-id="b0876-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="b0876-107">_wFlags_</span></span>
  
> <span data-ttu-id="b0876-108">Indica que o nome da chave que representa o fuso horário no registro do Windows é válido.</span><span class="sxs-lookup"><span data-stu-id="b0876-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="b0876-109">Como cada fuso horário sempre deve ser identificado por um nome de chave, esse membro sempre deve ter o valor **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="b0876-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="b0876-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="b0876-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="b0876-111">O nome da chave para este fuso horário no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="b0876-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="b0876-112">Esse nome não deve estar localizado.</span><span class="sxs-lookup"><span data-stu-id="b0876-112">This name must not be localized.</span></span> <span data-ttu-id="b0876-113">Ele tem um tamanho máximo de **MAX_PATH**, que é definida no Windows. arquivo de cabeçalho do Software Development Kit (SDK) do Windows h.</span><span class="sxs-lookup"><span data-stu-id="b0876-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="b0876-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="b0876-114">_cRules_</span></span>
  
> <span data-ttu-id="b0876-115">O número de regras para esta definição de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="b0876-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="b0876-116">O número máximo de regras é **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="b0876-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="b0876-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="b0876-117">_rgRules_</span></span>
  
> <span data-ttu-id="b0876-118">Uma matriz de regras que descrevem quando desloca ocorre.</span><span class="sxs-lookup"><span data-stu-id="b0876-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0876-119">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="b0876-119">Remarks</span></span>

<span data-ttu-id="b0876-120">Deve haver pelo menos uma regra *rgRules* .</span><span class="sxs-lookup"><span data-stu-id="b0876-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="b0876-121">A primeira regra no *rgRules* é considerado a regra usar até a segunda regra for iniciado, independentemente do *stStart* na primeira regra.</span><span class="sxs-lookup"><span data-stu-id="b0876-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="b0876-122">As regras devem ser classificadas do mais antigo para o mais recente.</span><span class="sxs-lookup"><span data-stu-id="b0876-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="b0876-123">Não há nenhuma sobreposição permitida entre as regras, portanto, uma regra anterior é considerada para encerrar quando inicia uma nova regra.</span><span class="sxs-lookup"><span data-stu-id="b0876-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0876-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0876-124">See also</span></span>

- [<span data-ttu-id="b0876-125">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="b0876-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="b0876-126">Sobre alteração de calendários por meio de programação para horário de verão</span><span class="sxs-lookup"><span data-stu-id="b0876-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="b0876-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="b0876-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)


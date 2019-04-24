---
title: SBitMaskRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBitMaskRestriction
api_type:
- COM
ms.assetid: ddd42180-6e4f-410c-9f78-d868a91452dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: afac8c352ad0a07fcb1cd98683b6a5c87940ab4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357523"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="28142-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="28142-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="28142-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28142-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28142-105">Descreve uma restrição de bitmask, que é usada para executar uma operação **e** bits e testar o resultado.</span><span class="sxs-lookup"><span data-stu-id="28142-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28142-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="28142-106">Header file:</span></span>  <br/> |<span data-ttu-id="28142-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="28142-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="28142-108">Members</span><span class="sxs-lookup"><span data-stu-id="28142-108">Members</span></span>

 <span data-ttu-id="28142-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="28142-109">**relBMR**</span></span>
  
> <span data-ttu-id="28142-110">Operador relacional que descreve como a máscara especificada no membro **ulMask** deve ser aplicada à marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="28142-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="28142-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="28142-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="28142-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="28142-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="28142-113">Execute uma operação **e** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para ser igual a zero.</span><span class="sxs-lookup"><span data-stu-id="28142-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="28142-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="28142-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="28142-115">Execute uma operação **e** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para não ser igual a zero.</span><span class="sxs-lookup"><span data-stu-id="28142-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="28142-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="28142-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="28142-117">Marca de propriedade da propriedade à qual a bitmask é aplicada.</span><span class="sxs-lookup"><span data-stu-id="28142-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="28142-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="28142-118">**ulMask**</span></span>
  
> <span data-ttu-id="28142-119">Bitmask a ser aplicado à propriedade identificada por **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="28142-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28142-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="28142-120">Remarks</span></span>

<span data-ttu-id="28142-121">A estrutura **SBitMaskRestriction** executa uma operação **e** bit a bit usando a bitmask descrita no membro **ulMask** e o valor da propriedade descrita pelo membro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="28142-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="28142-122">Se o resultado for zero, BMR_EQZ será satisfeito.</span><span class="sxs-lookup"><span data-stu-id="28142-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="28142-123">Se for diferente de zero, ou seja, se o valor da propriedade tiver pelo menos um dos mesmos bits definido como **ulMask**, então BMR_NEZ será satisfeito.</span><span class="sxs-lookup"><span data-stu-id="28142-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="28142-124">Para obter mais informações sobre a estrutura e as restrições do **SBitMaskRestriction** em geral, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="28142-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="28142-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="28142-125">See also</span></span>



[<span data-ttu-id="28142-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="28142-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="28142-127">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="28142-127">MAPI Structures</span></span>](mapi-structures.md)


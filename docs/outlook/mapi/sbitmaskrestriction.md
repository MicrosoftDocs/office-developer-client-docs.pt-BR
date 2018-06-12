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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: f0cf6fa03d8f38b7d160a8747111445cfdac1ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770296"
---
# <a name="sbitmaskrestriction"></a><span data-ttu-id="47bb9-103">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="47bb9-103">SBitMaskRestriction</span></span>

  
  
<span data-ttu-id="47bb9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47bb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47bb9-105">Descreve uma restrição de bitmask, que é usada para realizar uma operação de **AND** bit a bit e o resultado do teste.</span><span class="sxs-lookup"><span data-stu-id="47bb9-105">Describes a bitmask restriction, which is used to perform a bitwise **AND** operation and test the result.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47bb9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="47bb9-106">Header file:</span></span>  <br/> |<span data-ttu-id="47bb9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47bb9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBitMaskRestriction
{
  ULONG relBMR;
  PT_LONG ulPropTag;
  ULONG ulMask;
} SBitMaskRestriction;

```

## <a name="members"></a><span data-ttu-id="47bb9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="47bb9-108">Members</span></span>

 <span data-ttu-id="47bb9-109">**relBMR**</span><span class="sxs-lookup"><span data-stu-id="47bb9-109">**relBMR**</span></span>
  
> <span data-ttu-id="47bb9-110">Operador relacional que descreve como a máscara especificada no membro **ulMask** deve ser aplicada a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="47bb9-110">Relational operator that describes how the mask specified in the **ulMask** member should be applied to the property tag.</span></span> <span data-ttu-id="47bb9-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="47bb9-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="47bb9-112">BMR_EQZ</span><span class="sxs-lookup"><span data-stu-id="47bb9-112">BMR_EQZ</span></span> 
  
> <span data-ttu-id="47bb9-113">Execute uma operação **AND** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste de como sendo igual a zero.</span><span class="sxs-lookup"><span data-stu-id="47bb9-113">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being equal to zero.</span></span> 
    
<span data-ttu-id="47bb9-114">BMR_NEZ</span><span class="sxs-lookup"><span data-stu-id="47bb9-114">BMR_NEZ</span></span> 
  
> <span data-ttu-id="47bb9-115">Execute uma operação **AND** bit a bit da máscara no membro **ulMask** com a propriedade representada pelo membro **ulPropTag** e teste para não sendo igual a zero.</span><span class="sxs-lookup"><span data-stu-id="47bb9-115">Perform a bitwise **AND** operation of the mask in the **ulMask** member with the property represented by the **ulPropTag** member and test for being not equal to zero.</span></span> 
    
 <span data-ttu-id="47bb9-116">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="47bb9-116">**ulPropTag**</span></span>
  
> <span data-ttu-id="47bb9-117">Propriedade marca da propriedade à qual o bitmask é aplicado.</span><span class="sxs-lookup"><span data-stu-id="47bb9-117">Property tag of the property to which the bitmask is applied.</span></span>
    
 <span data-ttu-id="47bb9-118">**ulMask**</span><span class="sxs-lookup"><span data-stu-id="47bb9-118">**ulMask**</span></span>
  
> <span data-ttu-id="47bb9-119">Bitmask a ser aplicado à propriedade identificada pela **ulPropTag**.</span><span class="sxs-lookup"><span data-stu-id="47bb9-119">Bitmask to apply to the property identified by **ulPropTag**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47bb9-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="47bb9-120">Remarks</span></span>

<span data-ttu-id="47bb9-121">A estrutura **SBitMaskRestriction** executa uma operação **AND** bit a bit, usando o bitmask descrito no membro **ulMask** e o valor da propriedade descrito pelo membro **ulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="47bb9-121">The **SBitMaskRestriction** structure performs a bitwise **AND** operation using the bitmask described in the **ulMask** member and the value of the property described by the **ulPropTag** member.</span></span> <span data-ttu-id="47bb9-122">Se o resultado for zero, BMR_EQZ será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="47bb9-122">If the result is zero, BMR_EQZ is satisfied.</span></span> <span data-ttu-id="47bb9-123">Se for diferente de zero, ou seja, se o valor da propriedade tenha pelo menos uma dos mesmos bits definido como **ulMask**, em seguida, BMR_NEZ será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="47bb9-123">If it is nonzero, that is, if the property value has at least one of the same bits set as **ulMask**, then BMR_NEZ is satisfied.</span></span>
  
<span data-ttu-id="47bb9-124">Para obter mais informações sobre a estrutura de **SBitMaskRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="47bb9-124">For more information about the **SBitMaskRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="47bb9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="47bb9-125">See also</span></span>



[<span data-ttu-id="47bb9-126">SRestriction</span><span class="sxs-lookup"><span data-stu-id="47bb9-126">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="47bb9-127">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="47bb9-127">MAPI Structures</span></span>](mapi-structures.md)


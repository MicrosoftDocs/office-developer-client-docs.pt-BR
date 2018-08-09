---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770458"
---
# <a name="snotrestriction"></a><span data-ttu-id="55f3c-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="55f3c-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="55f3c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55f3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55f3c-105">Descreve uma restrição **não** , que é usada para aplicar uma operação **não é** lógica para uma restrição.</span><span class="sxs-lookup"><span data-stu-id="55f3c-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="55f3c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="55f3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="55f3c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55f3c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="55f3c-108">Members</span><span class="sxs-lookup"><span data-stu-id="55f3c-108">Members</span></span>

 <span data-ttu-id="55f3c-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="55f3c-109">**ulReserved**</span></span>
  
> <span data-ttu-id="55f3c-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="55f3c-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="55f3c-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="55f3c-111">**lpRes**</span></span>
  
> <span data-ttu-id="55f3c-112">Ponteiro para uma estrutura [SRestriction](srestriction.md) descrevendo a restrição de estar associado ao operador **não é** lógico.</span><span class="sxs-lookup"><span data-stu-id="55f3c-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="55f3c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55f3c-113">Remarks</span></span>

<span data-ttu-id="55f3c-114">Para obter mais informações sobre a estrutura **SNotRestriction** , consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="55f3c-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55f3c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="55f3c-115">See also</span></span>



[<span data-ttu-id="55f3c-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="55f3c-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="55f3c-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="55f3c-117">MAPI Structures</span></span>](mapi-structures.md)


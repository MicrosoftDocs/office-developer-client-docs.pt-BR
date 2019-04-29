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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426650"
---
# <a name="snotrestriction"></a><span data-ttu-id="57f9f-103">SNotRestriction</span><span class="sxs-lookup"><span data-stu-id="57f9f-103">SNotRestriction</span></span>

  
  
<span data-ttu-id="57f9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57f9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57f9f-105">Descreve uma restrição **not** , que é usada para aplicar uma operação lógica **not** a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="57f9f-105">Describes a **NOT** restriction, which is used to apply a logical **NOT** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57f9f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="57f9f-106">Header file:</span></span>  <br/> |<span data-ttu-id="57f9f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="57f9f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a><span data-ttu-id="57f9f-108">Members</span><span class="sxs-lookup"><span data-stu-id="57f9f-108">Members</span></span>

 <span data-ttu-id="57f9f-109">**ulReserved**</span><span class="sxs-lookup"><span data-stu-id="57f9f-109">**ulReserved**</span></span>
  
> <span data-ttu-id="57f9f-110">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="57f9f-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="57f9f-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="57f9f-111">**lpRes**</span></span>
  
> <span data-ttu-id="57f9f-112">Ponteiro para uma estrutura [SRestriction](srestriction.md) descrevendo a restrição a ser associada ao operador lógico **not** .</span><span class="sxs-lookup"><span data-stu-id="57f9f-112">Pointer to a [SRestriction](srestriction.md) structure describing the restriction to be joined to the logical **NOT** operator.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="57f9f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="57f9f-113">Remarks</span></span>

<span data-ttu-id="57f9f-114">Para obter mais informações sobre a estrutura **SNotRestriction** , consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="57f9f-114">For more information about the **SNotRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="57f9f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="57f9f-115">See also</span></span>



[<span data-ttu-id="57f9f-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="57f9f-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="57f9f-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="57f9f-117">MAPI Structures</span></span>](mapi-structures.md)


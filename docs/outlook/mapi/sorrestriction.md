---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437928"
---
# <a name="sorrestriction"></a><span data-ttu-id="21856-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="21856-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="21856-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21856-105">Descreve uma restrição **or** que é usada para aplicar uma operação **ou** lógica a uma restrição.</span><span class="sxs-lookup"><span data-stu-id="21856-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21856-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="21856-106">Header file:</span></span>  <br/> |<span data-ttu-id="21856-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="21856-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="21856-108">Members</span><span class="sxs-lookup"><span data-stu-id="21856-108">Members</span></span>

 <span data-ttu-id="21856-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="21856-109">**cRes**</span></span>
  
> <span data-ttu-id="21856-110">Contagem de estruturas na matriz apontada pelo membro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="21856-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="21856-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="21856-111">**lpRes**</span></span>
  
> <span data-ttu-id="21856-112">Ponteiro para a estrutura [SRestriction](srestriction.md) descrevendo a restrição a ser associada usando a operação **or** lógica.</span><span class="sxs-lookup"><span data-stu-id="21856-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="21856-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="21856-113">Remarks</span></span>

<span data-ttu-id="21856-114">Para obter mais informações sobre a estrutura **SOrRestriction** , consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="21856-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="21856-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="21856-115">See also</span></span>



[<span data-ttu-id="21856-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="21856-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="21856-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="21856-117">MAPI Structures</span></span>](mapi-structures.md)


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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770466"
---
# <a name="sorrestriction"></a><span data-ttu-id="8e5c3-103">SOrRestriction</span><span class="sxs-lookup"><span data-stu-id="8e5c3-103">SOrRestriction</span></span>

  
  
<span data-ttu-id="8e5c3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e5c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e5c3-105">Descreve uma restrição **ou** que é usada para aplicar uma operação **OR** lógica para uma restrição.</span><span class="sxs-lookup"><span data-stu-id="8e5c3-105">Describes an **OR** restriction which is used to apply a logical **OR** operation to a restriction.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e5c3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8e5c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="8e5c3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e5c3-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a><span data-ttu-id="8e5c3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8e5c3-108">Members</span></span>

 <span data-ttu-id="8e5c3-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="8e5c3-109">**cRes**</span></span>
  
> <span data-ttu-id="8e5c3-110">Contagem de estruturas na matriz apontado pelo membro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="8e5c3-110">Count of structures in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="8e5c3-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="8e5c3-111">**lpRes**</span></span>
  
> <span data-ttu-id="8e5c3-112">Ponteiro para a estrutura de [SRestriction](srestriction.md) descrevendo a restrição a serem agrupadas usando a operação **OR** lógica.</span><span class="sxs-lookup"><span data-stu-id="8e5c3-112">Pointer to the [SRestriction](srestriction.md) structure describing the restriction to be joined using the logical **OR** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8e5c3-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="8e5c3-113">Remarks</span></span>

<span data-ttu-id="8e5c3-114">Para obter mais informações sobre a estrutura **SOrRestriction** , consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="8e5c3-114">For more information about the **SOrRestriction** structure, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e5c3-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e5c3-115">See also</span></span>



[<span data-ttu-id="8e5c3-116">SRestriction</span><span class="sxs-lookup"><span data-stu-id="8e5c3-116">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="8e5c3-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="8e5c3-117">MAPI Structures</span></span>](mapi-structures.md)


---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438880"
---
# <a name="sandrestriction"></a><span data-ttu-id="97e93-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="97e93-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="97e93-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97e93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97e93-105">Descreve uma restrição **e** que é usada para ingressar em um grupo de restrições usando uma operação **e** lógica.</span><span class="sxs-lookup"><span data-stu-id="97e93-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97e93-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="97e93-106">Header file:</span></span>  <br/> |<span data-ttu-id="97e93-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="97e93-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="97e93-108">Members</span><span class="sxs-lookup"><span data-stu-id="97e93-108">Members</span></span>

 <span data-ttu-id="97e93-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="97e93-109">**cRes**</span></span>
  
> <span data-ttu-id="97e93-110">Contagem de restrições de pesquisa na matriz apontada pelo membro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="97e93-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="97e93-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="97e93-111">**lpRes**</span></span>
  
> <span data-ttu-id="97e93-112">Ponteiro para uma matriz de estruturas [SRestriction](srestriction.md) que serão combinadas com uma operação **e** lógica.</span><span class="sxs-lookup"><span data-stu-id="97e93-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="97e93-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="97e93-113">Remarks</span></span>

<span data-ttu-id="97e93-114">O resultado da **SAndRestriction** será true se todas as restrições filhas forem avaliadas como true.</span><span class="sxs-lookup"><span data-stu-id="97e93-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="97e93-115">É FALSE se qualquer restrição de filho é avaliada como FALSE.</span><span class="sxs-lookup"><span data-stu-id="97e93-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="97e93-116">Para obter uma descrição dos tipos de restrições, como criá-los e código de exemplo, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="97e93-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97e93-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="97e93-117">See also</span></span>



[<span data-ttu-id="97e93-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="97e93-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="97e93-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="97e93-119">MAPI Structures</span></span>](mapi-structures.md)


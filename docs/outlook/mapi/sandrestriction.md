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
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592322"
---
# <a name="sandrestriction"></a><span data-ttu-id="7a277-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="7a277-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="7a277-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a277-105">Descreve uma restrição **AND** , que é utilizada para ingressar em um grupo de restrições usando uma operação **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="7a277-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a277-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7a277-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a277-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a277-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="7a277-108">Members</span><span class="sxs-lookup"><span data-stu-id="7a277-108">Members</span></span>

 <span data-ttu-id="7a277-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="7a277-109">**cRes**</span></span>
  
> <span data-ttu-id="7a277-110">Contagem de restrições de pesquisa na matriz apontado pelo membro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="7a277-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="7a277-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="7a277-111">**lpRes**</span></span>
  
> <span data-ttu-id="7a277-112">Ponteiro para uma matriz de estruturas [SRestriction](srestriction.md) que será combinado com uma operação **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="7a277-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a277-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a277-113">Remarks</span></span>

<span data-ttu-id="7a277-114">O resultado do **SAndRestriction** é TRUE se todas as restrições de seu filho é avaliada como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7a277-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="7a277-115">Ele é FALSE se qualquer restrição de filhos for falso.</span><span class="sxs-lookup"><span data-stu-id="7a277-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="7a277-116">Para obter uma descrição dos tipos de restrições, como criá-los e código de exemplo, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7a277-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a277-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a277-117">See also</span></span>



[<span data-ttu-id="7a277-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7a277-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="7a277-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="7a277-119">MAPI Structures</span></span>](mapi-structures.md)


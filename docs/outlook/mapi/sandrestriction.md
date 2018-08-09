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
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770304"
---
# <a name="sandrestriction"></a><span data-ttu-id="10f0e-103">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="10f0e-103">SAndRestriction</span></span>

  
  
<span data-ttu-id="10f0e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10f0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10f0e-105">Descreve uma restrição **AND** , que é utilizada para ingressar em um grupo de restrições usando uma operação **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="10f0e-105">Describes an **AND** restriction, which is used to join a group of restrictions using a logical **AND** operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10f0e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="10f0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="10f0e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10f0e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a><span data-ttu-id="10f0e-108">Members</span><span class="sxs-lookup"><span data-stu-id="10f0e-108">Members</span></span>

 <span data-ttu-id="10f0e-109">**cRes**</span><span class="sxs-lookup"><span data-stu-id="10f0e-109">**cRes**</span></span>
  
> <span data-ttu-id="10f0e-110">Contagem de restrições de pesquisa na matriz apontado pelo membro **lpRes** .</span><span class="sxs-lookup"><span data-stu-id="10f0e-110">Count of search restrictions in the array pointed to by the **lpRes** member.</span></span> 
    
 <span data-ttu-id="10f0e-111">**lpRes**</span><span class="sxs-lookup"><span data-stu-id="10f0e-111">**lpRes**</span></span>
  
> <span data-ttu-id="10f0e-112">Ponteiro para uma matriz de estruturas [SRestriction](srestriction.md) que será combinado com uma operação **AND** lógica.</span><span class="sxs-lookup"><span data-stu-id="10f0e-112">Pointer to an array of [SRestriction](srestriction.md) structures that will be combined with a logical **AND** operation.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="10f0e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="10f0e-113">Remarks</span></span>

<span data-ttu-id="10f0e-114">O resultado do **SAndRestriction** é TRUE se todas as restrições de seu filho é avaliada como verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="10f0e-114">The result of the **SAndRestriction** is TRUE if all its child restrictions evaluate to TRUE.</span></span> <span data-ttu-id="10f0e-115">Ele é FALSE se qualquer restrição de filhos for falso.</span><span class="sxs-lookup"><span data-stu-id="10f0e-115">It is FALSE if any child restriction evaluates to FALSE.</span></span> 
  
<span data-ttu-id="10f0e-116">Para obter uma descrição dos tipos de restrições, como criá-los e código de exemplo, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="10f0e-116">For a description of types of restrictions, how to build them, and sample code, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10f0e-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="10f0e-117">See also</span></span>



[<span data-ttu-id="10f0e-118">SRestriction</span><span class="sxs-lookup"><span data-stu-id="10f0e-118">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="10f0e-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="10f0e-119">MAPI Structures</span></span>](mapi-structures.md)


---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438159"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="347ae-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="347ae-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="347ae-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="347ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="347ae-105">A estrutura é usada com [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="347ae-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="347ae-106">Members</span><span class="sxs-lookup"><span data-stu-id="347ae-106">Members</span></span>

 <span data-ttu-id="347ae-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="347ae-107">**ulSize**</span></span>
  
> <span data-ttu-id="347ae-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="347ae-108">The size of the structure.</span></span>
    
 <span data-ttu-id="347ae-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="347ae-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="347ae-110">Um ponteiro para o objeto IUnknown no qual este objeto está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="347ae-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="347ae-111">Isso permite que qualquer chamada de QueryInterface passe para o objeto criado.</span><span class="sxs-lookup"><span data-stu-id="347ae-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="347ae-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="347ae-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="347ae-113">Deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="347ae-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="347ae-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="347ae-114">See also</span></span>



[<span data-ttu-id="347ae-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="347ae-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="347ae-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="347ae-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)


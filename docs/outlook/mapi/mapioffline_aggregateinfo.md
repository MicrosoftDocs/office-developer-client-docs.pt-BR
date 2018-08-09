---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767996"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="cb70e-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="cb70e-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="cb70e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb70e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb70e-105">A estrutura é usada com [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="cb70e-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="cb70e-106">Members</span><span class="sxs-lookup"><span data-stu-id="cb70e-106">Members</span></span>

 <span data-ttu-id="cb70e-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="cb70e-107">**ulSize**</span></span>
  
> <span data-ttu-id="cb70e-108">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="cb70e-108">The size of the structure.</span></span>
    
 <span data-ttu-id="cb70e-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="cb70e-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="cb70e-110">Um ponteiro para o objeto IUnknown no qual esse objeto está sendo agregado.</span><span class="sxs-lookup"><span data-stu-id="cb70e-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="cb70e-111">Isso permite que as chamadas de QueryInterface a passagem para o objeto criado.</span><span class="sxs-lookup"><span data-stu-id="cb70e-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="cb70e-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="cb70e-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="cb70e-113">Deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="cb70e-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb70e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb70e-114">See also</span></span>



[<span data-ttu-id="cb70e-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="cb70e-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="cb70e-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="cb70e-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)


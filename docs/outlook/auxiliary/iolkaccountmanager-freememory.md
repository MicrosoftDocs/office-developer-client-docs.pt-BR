---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera memória alocada pela interface IOlkAccountManager.
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765956"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="235a2-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="235a2-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="235a2-104">Libera memória alocada pela interface [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="235a2-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="235a2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="235a2-105">Quick info</span></span>

<span data-ttu-id="235a2-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="235a2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="235a2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="235a2-107">Parameters</span></span>

<span data-ttu-id="235a2-108">_VP_</span><span class="sxs-lookup"><span data-stu-id="235a2-108">_pv_</span></span>
  
> <span data-ttu-id="235a2-109">[in] Um ponteiro para a memória para liberar.</span><span class="sxs-lookup"><span data-stu-id="235a2-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="235a2-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="235a2-110">Return values</span></span>

<span data-ttu-id="235a2-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="235a2-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="235a2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="235a2-112">Remarks</span></span>

<span data-ttu-id="235a2-113">Use esse método para liberar memória alocada pelo [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="235a2-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="235a2-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="235a2-114">See also</span></span>

- [<span data-ttu-id="235a2-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="235a2-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)


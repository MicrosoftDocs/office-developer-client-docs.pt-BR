---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: Libera memória alocada pela interface IOlkAccountManager.
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408485"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="ef586-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ef586-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="ef586-104">Libera memória alocada pela interface [IOlkAccountManager](iolkaccountmanager.md) .</span><span class="sxs-lookup"><span data-stu-id="ef586-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ef586-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ef586-105">Quick info</span></span>

<span data-ttu-id="ef586-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="ef586-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="ef586-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef586-107">Parameters</span></span>

<span data-ttu-id="ef586-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="ef586-108">_pv_</span></span>
  
> <span data-ttu-id="ef586-109">no Um ponteiro para a memória a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="ef586-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ef586-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ef586-110">Return values</span></span>

<span data-ttu-id="ef586-111">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="ef586-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef586-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef586-112">Remarks</span></span>

<span data-ttu-id="ef586-113">Use este método para liberar a memória alocada por [IOlkAccountManager:: GetOrder](iolkaccountmanager-getorder.md).</span><span class="sxs-lookup"><span data-stu-id="ef586-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef586-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef586-114">See also</span></span>

- [<span data-ttu-id="ef586-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="ef586-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)


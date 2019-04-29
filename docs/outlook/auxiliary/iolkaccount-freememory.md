---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera memória alocada pela interface IOlkAccount.
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406196"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="e6e53-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="e6e53-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="e6e53-104">Libera memória alocada pela interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e53-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e6e53-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="e6e53-105">Quick info</span></span>

<span data-ttu-id="e6e53-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="e6e53-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="e6e53-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6e53-107">Parameters</span></span>

<span data-ttu-id="e6e53-108">_PV_</span><span class="sxs-lookup"><span data-stu-id="e6e53-108">_pv_</span></span>
  
> <span data-ttu-id="e6e53-109">no Um ponteiro para que a memória seja liberada.</span><span class="sxs-lookup"><span data-stu-id="e6e53-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e6e53-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e6e53-110">Return values</span></span>

<span data-ttu-id="e6e53-111">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="e6e53-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6e53-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6e53-112">Remarks</span></span>

<span data-ttu-id="e6e53-113">Use este método para liberar memória alocada por [IOlkAccount:: GetProp](iolkaccount-getprop.md) (se o valor da propriedade de conta especificada for um tipo de cadeia de caracteres ou binário) e [IOlkAccount:: GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="e6e53-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6e53-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6e53-114">See also</span></span>

- [<span data-ttu-id="e6e53-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="e6e53-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="e6e53-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="e6e53-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)


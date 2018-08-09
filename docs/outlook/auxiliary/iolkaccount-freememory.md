---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: Libera memória alocada pela interface IOlkAccount.
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765900"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="2d93f-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="2d93f-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="2d93f-104">Libera memória alocada pela interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="2d93f-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2d93f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2d93f-105">Quick info</span></span>

<span data-ttu-id="2d93f-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2d93f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="2d93f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d93f-107">Parameters</span></span>

<span data-ttu-id="2d93f-108">_VP_</span><span class="sxs-lookup"><span data-stu-id="2d93f-108">_pv_</span></span>
  
> <span data-ttu-id="2d93f-109">[in] Um ponteiro para a memória para ser liberada.</span><span class="sxs-lookup"><span data-stu-id="2d93f-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="2d93f-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2d93f-110">Return values</span></span>

<span data-ttu-id="2d93f-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2d93f-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d93f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d93f-112">Remarks</span></span>

<span data-ttu-id="2d93f-113">Use este método para liberar memória alocado pelo [IOlkAccount::GetProp](iolkaccount-getprop.md) (se o valor da propriedade conta especificada é um tipo binário ou cadeia de caracteres) e [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span><span class="sxs-lookup"><span data-stu-id="2d93f-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d93f-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d93f-114">See also</span></span>

- [<span data-ttu-id="2d93f-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="2d93f-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="2d93f-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="2d93f-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)


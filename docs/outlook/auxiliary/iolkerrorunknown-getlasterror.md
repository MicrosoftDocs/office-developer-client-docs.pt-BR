---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtém uma cadeia de caracteres da mensagem de erro especificado.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765989"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="6e1f4-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6e1f4-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="6e1f4-104">Obtém uma cadeia de caracteres da mensagem de erro especificado.</span><span class="sxs-lookup"><span data-stu-id="6e1f4-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="6e1f4-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6e1f4-105">Quick info</span></span>

<span data-ttu-id="6e1f4-106">Consulte [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="6e1f4-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="6e1f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e1f4-107">Parameters</span></span>

<span data-ttu-id="6e1f4-108">_RH_</span><span class="sxs-lookup"><span data-stu-id="6e1f4-108">_hr_</span></span>
  
> <span data-ttu-id="6e1f4-109">[in] O código de erro a ser procurada.</span><span class="sxs-lookup"><span data-stu-id="6e1f4-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="6e1f4-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="6e1f4-110">_ppwszError_</span></span>
  
> <span data-ttu-id="6e1f4-111">[out] A mensagem de erro que corresponde ao *RH* .</span><span class="sxs-lookup"><span data-stu-id="6e1f4-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6e1f4-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6e1f4-112">Return values</span></span>

|<span data-ttu-id="6e1f4-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6e1f4-113">**HRESULT**</span></span>|<span data-ttu-id="6e1f4-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6e1f4-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6e1f4-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e1f4-115">S_OK</span></span>  <br/> |<span data-ttu-id="6e1f4-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6e1f4-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6e1f4-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6e1f4-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="6e1f4-118">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="6e1f4-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e1f4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e1f4-119">See also</span></span>

- [<span data-ttu-id="6e1f4-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="6e1f4-120">Constants (Account management API)</span></span>](constants-account-management-api.md)


---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtém uma cadeia de caracteres de mensagem para o erro especificado.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431698"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="a35ed-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a35ed-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="a35ed-104">Obtém uma cadeia de caracteres de mensagem para o erro especificado.</span><span class="sxs-lookup"><span data-stu-id="a35ed-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a35ed-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a35ed-105">Quick info</span></span>

<span data-ttu-id="a35ed-106">Consulte [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a35ed-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="a35ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a35ed-107">Parameters</span></span>

<span data-ttu-id="a35ed-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="a35ed-108">_hr_</span></span>
  
> <span data-ttu-id="a35ed-109">[in] O código de erro a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="a35ed-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="a35ed-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="a35ed-110">_ppwszError_</span></span>
  
> <span data-ttu-id="a35ed-111">[out] A mensagem de erro que corresponde ao  *rh*  .</span><span class="sxs-lookup"><span data-stu-id="a35ed-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="a35ed-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="a35ed-112">Return values</span></span>

|<span data-ttu-id="a35ed-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a35ed-113">**HRESULT**</span></span>|<span data-ttu-id="a35ed-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a35ed-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a35ed-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a35ed-115">S_OK</span></span>  <br/> |<span data-ttu-id="a35ed-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a35ed-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="a35ed-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a35ed-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a35ed-118">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="a35ed-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a35ed-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a35ed-119">See also</span></span>

- [<span data-ttu-id="a35ed-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="a35ed-120">Constants (Account management API)</span></span>](constants-account-management-api.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321879"
---
# <a name="iolkerrorunknowngetlasterror"></a><span data-ttu-id="254bb-103">IOlkErrorUnknown::GetLastError</span><span class="sxs-lookup"><span data-stu-id="254bb-103">IOlkErrorUnknown::GetLastError</span></span>

<span data-ttu-id="254bb-104">Obtém uma cadeia de caracteres de mensagem para o erro especificado.</span><span class="sxs-lookup"><span data-stu-id="254bb-104">Gets a message string for the specified error.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="254bb-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="254bb-105">Quick info</span></span>

<span data-ttu-id="254bb-106">Consulte [IOlkErrorUnknown](iolkerrorunknown.md).</span><span class="sxs-lookup"><span data-stu-id="254bb-106">See [IOlkErrorUnknown](iolkerrorunknown.md).</span></span>
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a><span data-ttu-id="254bb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="254bb-107">Parameters</span></span>

<span data-ttu-id="254bb-108">_hr_</span><span class="sxs-lookup"><span data-stu-id="254bb-108">_hr_</span></span>
  
> <span data-ttu-id="254bb-109">no O código de erro a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="254bb-109">[in] The error code to look up.</span></span>
    
<span data-ttu-id="254bb-110">_ppwszError_</span><span class="sxs-lookup"><span data-stu-id="254bb-110">_ppwszError_</span></span>
  
> <span data-ttu-id="254bb-111">bota A mensagem de erro que corresponde ao *HR* .</span><span class="sxs-lookup"><span data-stu-id="254bb-111">[out] The error message that corresponds to  *hr*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="254bb-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="254bb-112">Return values</span></span>

|<span data-ttu-id="254bb-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="254bb-113">**HRESULT**</span></span>|<span data-ttu-id="254bb-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="254bb-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="254bb-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="254bb-115">S_OK</span></span>  <br/> |<span data-ttu-id="254bb-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="254bb-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="254bb-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="254bb-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="254bb-118">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="254bb-118">One or more arguments are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="254bb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="254bb-119">See also</span></span>

- [<span data-ttu-id="254bb-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="254bb-120">Constants (Account management API)</span></span>](constants-account-management-api.md)


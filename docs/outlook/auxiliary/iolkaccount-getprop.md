---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtém o valor da propriedade de conta especificada.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433735"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="6744a-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="6744a-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="6744a-104">Obtém o valor da propriedade de conta especificada.</span><span class="sxs-lookup"><span data-stu-id="6744a-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6744a-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6744a-105">Quick info</span></span>

<span data-ttu-id="6744a-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="6744a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="6744a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6744a-107">Parameters</span></span>

<span data-ttu-id="6744a-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="6744a-108">_dwProp_</span></span>
  
> <span data-ttu-id="6744a-109">no A marca de propriedade da propriedade Account a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="6744a-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="6744a-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="6744a-110">_pVar_</span></span>
  
> <span data-ttu-id="6744a-111">bota O valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="6744a-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="6744a-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6744a-112">Return values</span></span>

|<span data-ttu-id="6744a-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6744a-113">**HRESULT**</span></span>|<span data-ttu-id="6744a-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6744a-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6744a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="6744a-115">S_OK</span></span>  <br/> |<span data-ttu-id="6744a-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6744a-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6744a-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6744a-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="6744a-118">A propriedade não é encontrada para a conta determinada.</span><span class="sxs-lookup"><span data-stu-id="6744a-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="6744a-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6744a-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="6744a-120">Uma marca de propriedade inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="6744a-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6744a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6744a-121">Remarks</span></span>

<span data-ttu-id="6744a-122">Depois que esse método retornar, se o valor da propriedade Account for um tipo de cadeia de caracteres ou binário, você deverá liberar *pvar* usando [IOlkAccount:: freememory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="6744a-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6744a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6744a-123">See also</span></span>

- [<span data-ttu-id="6744a-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="6744a-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="6744a-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="6744a-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="6744a-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="6744a-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)


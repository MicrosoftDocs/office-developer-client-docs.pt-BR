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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321228"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="8531b-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="8531b-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="8531b-104">Obtém o valor da propriedade de conta especificada.</span><span class="sxs-lookup"><span data-stu-id="8531b-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8531b-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8531b-105">Quick info</span></span>

<span data-ttu-id="8531b-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8531b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="8531b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8531b-107">Parameters</span></span>

<span data-ttu-id="8531b-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="8531b-108">_dwProp_</span></span>
  
> <span data-ttu-id="8531b-109">no A marca de propriedade da propriedade Account a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8531b-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="8531b-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="8531b-110">_pVar_</span></span>
  
> <span data-ttu-id="8531b-111">bota O valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="8531b-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8531b-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8531b-112">Return values</span></span>

|<span data-ttu-id="8531b-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8531b-113">**HRESULT**</span></span>|<span data-ttu-id="8531b-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8531b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8531b-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8531b-115">S_OK</span></span>  <br/> |<span data-ttu-id="8531b-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8531b-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="8531b-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8531b-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8531b-118">A propriedade não é encontrada para a conta determinada.</span><span class="sxs-lookup"><span data-stu-id="8531b-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="8531b-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8531b-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8531b-120">Uma marca de propriedade inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="8531b-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8531b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8531b-121">Remarks</span></span>

<span data-ttu-id="8531b-122">Depois que esse método retornar, se o valor da propriedade Account for um tipo de cadeia de caracteres ou binário, você deverá liberar *pvar* usando [IOlkAccount:: freememory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="8531b-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8531b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8531b-123">See also</span></span>

- [<span data-ttu-id="8531b-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="8531b-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="8531b-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="8531b-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="8531b-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="8531b-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)


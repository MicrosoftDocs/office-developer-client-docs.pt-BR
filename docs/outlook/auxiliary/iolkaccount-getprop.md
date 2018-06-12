---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtém o valor da propriedade conta especificada.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765908"
---
# <a name="iolkaccountgetprop"></a><span data-ttu-id="2cb7f-103">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="2cb7f-103">IOlkAccount::GetProp</span></span>

<span data-ttu-id="2cb7f-104">Obtém o valor da propriedade conta especificada.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-104">Gets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2cb7f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2cb7f-105">Quick info</span></span>

<span data-ttu-id="2cb7f-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2cb7f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="2cb7f-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2cb7f-107">Parameters</span></span>

<span data-ttu-id="2cb7f-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="2cb7f-108">_dwProp_</span></span>
  
> <span data-ttu-id="2cb7f-109">[in] A marca de propriedade da propriedade a conta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-109">[in] The property tag of the account property to get.</span></span>
    
<span data-ttu-id="2cb7f-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="2cb7f-110">_pVar_</span></span>
  
> <span data-ttu-id="2cb7f-111">[out] O valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-111">[out] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="2cb7f-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2cb7f-112">Return values</span></span>

|<span data-ttu-id="2cb7f-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2cb7f-113">**HRESULT**</span></span>|<span data-ttu-id="2cb7f-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2cb7f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2cb7f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="2cb7f-115">S_OK</span></span>  <br/> |<span data-ttu-id="2cb7f-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="2cb7f-117">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2cb7f-117">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="2cb7f-118">A propriedade não foi encontrada para a conta de determinado.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-118">The property is not found for the given account.</span></span>  <br/> |
|<span data-ttu-id="2cb7f-119">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2cb7f-119">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="2cb7f-120">Uma marca de propriedade inválido foi especificada.</span><span class="sxs-lookup"><span data-stu-id="2cb7f-120">An invalid property tag has been specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cb7f-121">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2cb7f-121">Remarks</span></span>

<span data-ttu-id="2cb7f-122">Depois que esse método retorna, se o valor da propriedade conta é um tipo binário ou cadeia de caracteres, você deve liberar *pVar* usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="2cb7f-122">After this method returns, if the value of the account property is a binary or string type, you must free  *pVar*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cb7f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cb7f-123">See also</span></span>

- [<span data-ttu-id="2cb7f-124">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="2cb7f-124">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="2cb7f-125">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="2cb7f-125">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)  
- [<span data-ttu-id="2cb7f-126">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="2cb7f-126">IOlkAccount::SetProp</span></span>](iolkaccount-setprop.md)


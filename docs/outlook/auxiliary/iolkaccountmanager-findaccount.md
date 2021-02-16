---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: Localiza uma conta por valor de propriedade.
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428799"
---
# <a name="iolkaccountmanagerfindaccount"></a><span data-ttu-id="6a0c8-103">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="6a0c8-103">IOlkAccountManager::FindAccount</span></span>

<span data-ttu-id="6a0c8-104">Localiza uma conta por valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-104">Finds an account by property value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6a0c8-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6a0c8-105">Quick info</span></span>

<span data-ttu-id="6a0c8-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="6a0c8-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a><span data-ttu-id="6a0c8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a0c8-107">Parameters</span></span>

<span data-ttu-id="6a0c8-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-108">_dwProp_</span></span>
  
> <span data-ttu-id="6a0c8-109">[in] A propriedade a ser pesquisada.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-109">[in] The property to search on.</span></span> <span data-ttu-id="6a0c8-110">Deve ser [PROP_ACCT_ID](prop_acct_id.md) ou [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span><span class="sxs-lookup"><span data-stu-id="6a0c8-110">Must be [PROP_ACCT_ID](prop_acct_id.md) or [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md).</span></span>
    
<span data-ttu-id="6a0c8-111">_pVar_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-111">_pVar_</span></span>
  
> <span data-ttu-id="6a0c8-112">[in] O valor a ser corresponder.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-112">[in] The value to match.</span></span>
    
<span data-ttu-id="6a0c8-113">_ppAccount_</span><span class="sxs-lookup"><span data-stu-id="6a0c8-113">_ppAccount_</span></span>
  
> <span data-ttu-id="6a0c8-114">[out] A conta encontrada.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-114">[out] The account found.</span></span> <span data-ttu-id="6a0c8-115">Esse objeto dá suporte a uma interface [IOlkAccount.](iolkaccount.md)</span><span class="sxs-lookup"><span data-stu-id="6a0c8-115">This object supports an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6a0c8-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6a0c8-116">Return values</span></span>

|<span data-ttu-id="6a0c8-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-117">**HRESULT**</span></span>|<span data-ttu-id="6a0c8-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6a0c8-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a0c8-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a0c8-119">S_OK</span></span>  <br/> |<span data-ttu-id="6a0c8-120">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6a0c8-121">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6a0c8-121">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="6a0c8-122">A conta especificada não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-122">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="6a0c8-123">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="6a0c8-123">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="6a0c8-124">O gerenciador de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-124">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="6a0c8-125">E_OLK_PARAM_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="6a0c8-125">E_OLK_PARAM_NOT_SUPPORTED</span></span>  <br/> |<span data-ttu-id="6a0c8-126">Um ou mais parâmetros são inválidos.</span><span class="sxs-lookup"><span data-stu-id="6a0c8-126">One or more parameters are invalid.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a0c8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a0c8-127">See also</span></span>

- [<span data-ttu-id="6a0c8-128">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="6a0c8-128">ACCT_VARIANT</span></span>](acct_variant.md)  
- [<span data-ttu-id="6a0c8-129">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="6a0c8-129">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="6a0c8-130">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="6a0c8-130">IOlkAccountHelper</span></span>](iolkaccounthelper.md)


---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtém as informações de tipo e categorias para a conta especificada.
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765891"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="4f2d8-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="4f2d8-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="4f2d8-104">Obtém as informações de tipo e categorias para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4f2d8-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4f2d8-105">Quick info</span></span>

<span data-ttu-id="4f2d8-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4f2d8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="4f2d8-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="4f2d8-107">Parameters</span></span>

<span data-ttu-id="4f2d8-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="4f2d8-108">_pclsidType_</span></span>
  
> <span data-ttu-id="4f2d8-109">[out] O identificador de classe do tipo de conta.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="4f2d8-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="4f2d8-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="4f2d8-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="4f2d8-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="4f2d8-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="4f2d8-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="4f2d8-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="4f2d8-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="4f2d8-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="4f2d8-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="4f2d8-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="4f2d8-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="4f2d8-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="4f2d8-116">_pcCategories_</span></span>
  
> <span data-ttu-id="4f2d8-117">[out] O número de categorias no _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="4f2d8-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="4f2d8-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="4f2d8-119">[out] Uma matriz das categorias que essa conta está associada.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="4f2d8-120">A matriz é do tamanho \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="4f2d8-121">O valor de cada categoria na matriz deve ser um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="4f2d8-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="4f2d8-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="4f2d8-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="4f2d8-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="4f2d8-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="4f2d8-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="4f2d8-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4f2d8-125">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="4f2d8-125">Return values</span></span>

<span data-ttu-id="4f2d8-126">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f2d8-127">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4f2d8-127">Remarks</span></span>

<span data-ttu-id="4f2d8-128">Depois que esse método retorna, você deve liberar *prgclsidCategory* usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="4f2d8-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="4f2d8-129">**IOlkAccount::GetAccountInfo** não oferece suporte a categoria do catálogo de endereços para uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="4f2d8-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="4f2d8-130">Se a conta for uma troca conta (*pclsidType* é **CLSID_OlkMAPIAccount** ) e a conta implementa o catálogo de endereços, chamada **IOlkAccount::GetAccountInfo** não retornará **CLSID_OlkAddressBook** como uma categoria no * prgclsidCategory* .</span><span class="sxs-lookup"><span data-stu-id="4f2d8-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f2d8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f2d8-131">See also</span></span>

- [<span data-ttu-id="4f2d8-132">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="4f2d8-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="4f2d8-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="4f2d8-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)


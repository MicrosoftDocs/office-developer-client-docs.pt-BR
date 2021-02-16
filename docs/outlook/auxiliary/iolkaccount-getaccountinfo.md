---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtém as informações de tipo e categorias da conta especificada.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437900"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="aebb5-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="aebb5-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="aebb5-104">Obtém as informações de tipo e categorias da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="aebb5-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aebb5-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aebb5-105">Quick info</span></span>

<span data-ttu-id="aebb5-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="aebb5-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="aebb5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aebb5-107">Parameters</span></span>

<span data-ttu-id="aebb5-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="aebb5-108">_pclsidType_</span></span>
  
> <span data-ttu-id="aebb5-109">[out] O identificador de classe para o tipo de conta.</span><span class="sxs-lookup"><span data-stu-id="aebb5-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="aebb5-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="aebb5-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="aebb5-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="aebb5-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="aebb5-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="aebb5-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="aebb5-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="aebb5-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="aebb5-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="aebb5-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="aebb5-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="aebb5-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="aebb5-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="aebb5-116">_pcCategories_</span></span>
  
> <span data-ttu-id="aebb5-117">[out] O número de categorias  _em prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="aebb5-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="aebb5-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="aebb5-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="aebb5-119">[out] Uma matriz de categorias às que esta conta está associada.</span><span class="sxs-lookup"><span data-stu-id="aebb5-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="aebb5-120">A matriz tem o tamanho \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="aebb5-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="aebb5-121">O valor de cada categoria na matriz deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="aebb5-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="aebb5-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="aebb5-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="aebb5-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="aebb5-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="aebb5-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="aebb5-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="aebb5-125">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aebb5-125">Return values</span></span>

<span data-ttu-id="aebb5-126">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="aebb5-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aebb5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="aebb5-127">Remarks</span></span>

<span data-ttu-id="aebb5-128">Depois que esse método retornar, você deverá liberar  *prgclsidCategory*  usando [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="aebb5-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="aebb5-129">**IOlkAccount::GetAccountInfo** não dá suporte à categoria de livro de endereços de uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="aebb5-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="aebb5-130">Se a conta for uma conta do Exchange (*pclsidType*  é **CLSID_OlkMAPIAccount** ), e a conta implementa o livro de endereços, chamar **IOlkAccount::GetAccountInfo** não retornará **CLSID_OlkAddressBook** como uma categoria em  *prgclsidCategory*  .</span><span class="sxs-lookup"><span data-stu-id="aebb5-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aebb5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="aebb5-131">See also</span></span>

- [<span data-ttu-id="aebb5-132">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="aebb5-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="aebb5-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="aebb5-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)


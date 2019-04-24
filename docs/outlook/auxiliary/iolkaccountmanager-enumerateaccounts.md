---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtém um enumerador para as contas da categoria ou tipo específico.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322047"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="1450d-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="1450d-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="1450d-104">Obtém um enumerador para as contas da categoria ou tipo específico.</span><span class="sxs-lookup"><span data-stu-id="1450d-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1450d-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1450d-105">Quick info</span></span>

<span data-ttu-id="1450d-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="1450d-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="1450d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1450d-107">Parameters</span></span>

<span data-ttu-id="1450d-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="1450d-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="1450d-109">no O identificador de classe da categoria a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="1450d-109">[in] The class identifier of the category to enumerate.</span></span> <span data-ttu-id="1450d-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="1450d-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="1450d-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="1450d-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="1450d-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="1450d-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="1450d-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="1450d-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="1450d-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="1450d-114">_pclsidType_</span></span>
  
> <span data-ttu-id="1450d-115">no O identificador de classe do tipo de conta a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="1450d-115">[in] The class identifier of the account type to enumerate.</span></span> <span data-ttu-id="1450d-116">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="1450d-116">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="1450d-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="1450d-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="1450d-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="1450d-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="1450d-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="1450d-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="1450d-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="1450d-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="1450d-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="1450d-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="1450d-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="1450d-122">_dwFlags_</span></span>
  
> <span data-ttu-id="1450d-123">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="1450d-123">[in] Flags to modify behavior.</span></span> <span data-ttu-id="1450d-124">O único valor com suporte é OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="1450d-124">The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="1450d-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="1450d-125">_ppEnum_</span></span>
  
> <span data-ttu-id="1450d-126">bota Um enumerador que oferece suporte à interface [IOlkEnum](iolkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="1450d-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1450d-127">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1450d-127">Return values</span></span>

|<span data-ttu-id="1450d-128">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1450d-128">**HRESULT**</span></span>|<span data-ttu-id="1450d-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1450d-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1450d-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="1450d-130">S_OK</span></span>  <br/> |<span data-ttu-id="1450d-131">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1450d-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="1450d-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="1450d-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="1450d-133">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="1450d-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1450d-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="1450d-134">Remarks</span></span>

<span data-ttu-id="1450d-135">Especificar NULL para Category retorna um enumerador de todas as contas do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1450d-135">Specifying NULL for category returns an enumerator of all accounts of the specified type.</span></span> <span data-ttu-id="1450d-136">Da mesma forma, especificar NULL para Type retorna um enumerador de todas as contas da categoria especificada.</span><span class="sxs-lookup"><span data-stu-id="1450d-136">Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="1450d-137">**IOlkAccountManager:: EnumerateAccounts** não dá suporte à categoria catálogo de endereços para uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="1450d-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="1450d-138">Se a conta for uma conta do Exchange (*pclsidType* é **CLSID_OlkMAPIAccount** ) e você estiver tentando enumerar contas que implementam o catálogo de endereços (*prgclsidCategory* é **CLSID_OlkAddressBook** ), chamar \*\* IOlkAccountManager:: EnumerateAccounts\*\* não retornará a conta do Exchange no enumerador de contas *ppEnum* .</span><span class="sxs-lookup"><span data-stu-id="1450d-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1450d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="1450d-139">See also</span></span>

- [<span data-ttu-id="1450d-140">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="1450d-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="1450d-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="1450d-141">IOlkEnum</span></span>](iolkenum.md)


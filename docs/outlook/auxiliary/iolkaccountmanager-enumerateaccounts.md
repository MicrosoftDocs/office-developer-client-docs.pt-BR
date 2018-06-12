---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtém um enumerador para as contas do tipo ou categoria específica.
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765963"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="5aa3f-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="5aa3f-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="5aa3f-104">Obtém um enumerador para as contas do tipo ou categoria específica.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5aa3f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5aa3f-105">Quick info</span></span>

<span data-ttu-id="5aa3f-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="5aa3f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="5aa3f-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5aa3f-107">Parameters</span></span>

<span data-ttu-id="5aa3f-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="5aa3f-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="5aa3f-109">[in] O identificador de classe da categoria para enumerar.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-109">[in] The class identifier of the category to enumerate.</span></span> <span data-ttu-id="5aa3f-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="5aa3f-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="5aa3f-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="5aa3f-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="5aa3f-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="5aa3f-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="5aa3f-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="5aa3f-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="5aa3f-114">_pclsidType_</span></span>
  
> <span data-ttu-id="5aa3f-115">[in] O identificador de classe do tipo de conta para enumerar.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-115">[in] The class identifier of the account type to enumerate.</span></span> <span data-ttu-id="5aa3f-116">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="5aa3f-116">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="5aa3f-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="5aa3f-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="5aa3f-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="5aa3f-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="5aa3f-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="5aa3f-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="5aa3f-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="5aa3f-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="5aa3f-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="5aa3f-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="5aa3f-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5aa3f-122">_dwFlags_</span></span>
  
> <span data-ttu-id="5aa3f-123">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-123">[in] Flags to modify behavior.</span></span> <span data-ttu-id="5aa3f-124">O único valor com suporte é OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-124">The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="5aa3f-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="5aa3f-125">_ppEnum_</span></span>
  
> <span data-ttu-id="5aa3f-126">[out] Um enumerador que dá suporte à interface [IOlkEnum](iolkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa3f-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5aa3f-127">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5aa3f-127">Return values</span></span>

|<span data-ttu-id="5aa3f-128">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5aa3f-128">**HRESULT**</span></span>|<span data-ttu-id="5aa3f-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5aa3f-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5aa3f-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="5aa3f-130">S_OK</span></span>  <br/> |<span data-ttu-id="5aa3f-131">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="5aa3f-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="5aa3f-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="5aa3f-133">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5aa3f-134">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5aa3f-134">Remarks</span></span>

<span data-ttu-id="5aa3f-135">Especificando NULL para categoria retorna um enumerador de todas as contas do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-135">Specifying NULL for category returns an enumerator of all accounts of the specified type.</span></span> <span data-ttu-id="5aa3f-136">Da mesma forma, especificando NULL para tipo retorna um enumerador de todas as contas da categoria especificada.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-136">Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="5aa3f-137">**IOlkAccountManager::EnumerateAccounts** não oferece suporte a categoria do catálogo de endereços para uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="5aa3f-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="5aa3f-138">Se a conta for uma conta do Exchange (*pclsidType* é **CLSID_OlkMAPIAccount** ), e você está tentando enumerar contas que implementam o catálogo de endereços (*prgclsidCategory* é **CLSID_OlkAddressBook** ), chamar ** IOlkAccountManager::EnumerateAccounts** não retornará a conta do Exchange no enumerador de contas *ppEnum* .</span><span class="sxs-lookup"><span data-stu-id="5aa3f-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5aa3f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5aa3f-139">See also</span></span>

- [<span data-ttu-id="5aa3f-140">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="5aa3f-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="5aa3f-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="5aa3f-141">IOlkEnum</span></span>](iolkenum.md)


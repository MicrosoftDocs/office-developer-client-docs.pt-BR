---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma as alterações no objeto Account gravando no repositório do registro.
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322257"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="02ffe-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="02ffe-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="02ffe-104">Confirma as alterações no objeto Account gravando no repositório do registro.</span><span class="sxs-lookup"><span data-stu-id="02ffe-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="02ffe-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="02ffe-105">Quick info</span></span>

<span data-ttu-id="02ffe-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="02ffe-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="02ffe-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02ffe-107">Parameters</span></span>

<span data-ttu-id="02ffe-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="02ffe-108">_dwFlags_</span></span>
  
> <span data-ttu-id="02ffe-109">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="02ffe-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="02ffe-110">OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="02ffe-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="02ffe-111">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="02ffe-111">Return values</span></span>

|<span data-ttu-id="02ffe-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="02ffe-112">**HRESULT**</span></span>|<span data-ttu-id="02ffe-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02ffe-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02ffe-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="02ffe-114">S_OK</span></span>  <br/> |<span data-ttu-id="02ffe-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="02ffe-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="02ffe-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="02ffe-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="02ffe-117">Não é possível localizar a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="02ffe-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="02ffe-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="02ffe-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="02ffe-119">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="02ffe-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02ffe-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="02ffe-120">Remarks</span></span>

<span data-ttu-id="02ffe-121">Após alterar o valor das propriedades da conta usando [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccount:: SaveChanges** para salvar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="02ffe-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02ffe-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="02ffe-122">See also</span></span>

- [<span data-ttu-id="02ffe-123">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="02ffe-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="02ffe-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="02ffe-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)


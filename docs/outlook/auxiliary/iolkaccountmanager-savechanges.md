---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Salva as alterações na conta especificada.
ms.openlocfilehash: dbb1dffa1725e96bd2ab635341718ce53738b864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322019"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="8784a-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8784a-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="8784a-104">Salva as alterações na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="8784a-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8784a-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8784a-105">Quick info</span></span>

<span data-ttu-id="8784a-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="8784a-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="8784a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8784a-107">Parameters</span></span>

<span data-ttu-id="8784a-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="8784a-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="8784a-109">no A ID da conta a ser salva.</span><span class="sxs-lookup"><span data-stu-id="8784a-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="8784a-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8784a-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8784a-111">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="8784a-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="8784a-112">OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="8784a-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8784a-113">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8784a-113">Return values</span></span>

|<span data-ttu-id="8784a-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8784a-114">**HRESULT**</span></span>|<span data-ttu-id="8784a-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8784a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8784a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8784a-116">S_OK</span></span>  <br/> |<span data-ttu-id="8784a-117">A chamada teve êxito</span><span class="sxs-lookup"><span data-stu-id="8784a-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="8784a-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8784a-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="8784a-119">A conta especificada não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="8784a-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="8784a-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8784a-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="8784a-121">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="8784a-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8784a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8784a-122">Remarks</span></span>

<span data-ttu-id="8784a-123">Após alterar o valor das propriedades da conta usando [IOlkAccount:: SetProp](iolkaccount-setprop.md), use **IOlkAccountManager:: SaveChanges** ou [IOlkAccount::](iolkaccount-savechanges.md) SaveChanges para salvar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="8784a-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8784a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8784a-124">See also</span></span>

- [<span data-ttu-id="8784a-125">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="8784a-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="8784a-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8784a-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)


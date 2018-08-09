---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: Salva as alterações para a conta especificada.
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765976"
---
# <a name="iolkaccountmanagersavechanges"></a><span data-ttu-id="db615-103">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="db615-103">IOlkAccountManager::SaveChanges</span></span>

<span data-ttu-id="db615-104">Salva as alterações para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="db615-104">Saves changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db615-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="db615-105">Quick info</span></span>

<span data-ttu-id="db615-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="db615-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="db615-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db615-107">Parameters</span></span>

<span data-ttu-id="db615-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="db615-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="db615-109">[in] A ID de conta para salvar.</span><span class="sxs-lookup"><span data-stu-id="db615-109">[in] The account ID to save.</span></span> 
    
<span data-ttu-id="db615-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="db615-110">_dwFlags_</span></span>
  
> <span data-ttu-id="db615-111">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="db615-111">[in] Flags to modify behavior.</span></span> <span data-ttu-id="db615-112">OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="db615-112">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="db615-113">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="db615-113">Return values</span></span>

|<span data-ttu-id="db615-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db615-114">**HRESULT**</span></span>|<span data-ttu-id="db615-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="db615-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db615-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="db615-116">S_OK</span></span>  <br/> |<span data-ttu-id="db615-117">A chamada foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="db615-117">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="db615-118">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="db615-118">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="db615-119">A conta especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="db615-119">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="db615-120">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="db615-120">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="db615-121">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="db615-121">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db615-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="db615-122">Remarks</span></span>

<span data-ttu-id="db615-123">Após alterar o valor das propriedades de conta usando [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** ou [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="db615-123">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccountManager::SaveChanges** or [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="db615-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="db615-124">See also</span></span>

- [<span data-ttu-id="db615-125">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="db615-125">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="db615-126">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="db615-126">IOlkAccount::SaveChanges</span></span>](iolkaccount-savechanges.md)


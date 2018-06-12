---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: Confirma as alterações para o objeto account escrevendo no repositório de registro.
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765906"
---
# <a name="iolkaccountsavechanges"></a><span data-ttu-id="08e72-103">IOlkAccount::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="08e72-103">IOlkAccount::SaveChanges</span></span>

<span data-ttu-id="08e72-104">Confirma as alterações para o objeto account escrevendo no repositório de registro.</span><span class="sxs-lookup"><span data-stu-id="08e72-104">Commits changes to the account object by writing to the registry store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="08e72-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="08e72-105">Quick info</span></span>

<span data-ttu-id="08e72-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="08e72-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a><span data-ttu-id="08e72-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="08e72-107">Parameters</span></span>

<span data-ttu-id="08e72-108">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="08e72-108">_dwFlags_</span></span>
  
> <span data-ttu-id="08e72-109">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="08e72-109">[in] Flags to modify behavior.</span></span> <span data-ttu-id="08e72-110">OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="08e72-110">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="08e72-111">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="08e72-111">Return values</span></span>

|<span data-ttu-id="08e72-112">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="08e72-112">**HRESULT**</span></span>|<span data-ttu-id="08e72-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="08e72-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08e72-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="08e72-114">S_OK</span></span>  <br/> |<span data-ttu-id="08e72-115">O método foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="08e72-115">The method was successful.</span></span>  <br/> |
|<span data-ttu-id="08e72-116">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="08e72-116">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="08e72-117">Não é possível localizar a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="08e72-117">Cannot find the specified account.</span></span>  <br/> |
|<span data-ttu-id="08e72-118">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="08e72-118">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="08e72-119">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="08e72-119">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08e72-120">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="08e72-120">Remarks</span></span>

<span data-ttu-id="08e72-121">Após alterar o valor das propriedades de conta usando [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** salve as alterações.</span><span class="sxs-lookup"><span data-stu-id="08e72-121">After changing the value of account properties by using [IOlkAccount::SetProp](iolkaccount-setprop.md), use **IOlkAccount::SaveChanges** to save such changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08e72-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="08e72-122">See also</span></span>

- [<span data-ttu-id="08e72-123">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="08e72-123">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="08e72-124">IOlkAccountManager::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="08e72-124">IOlkAccountManager::SaveChanges</span></span>](iolkaccountmanager-savechanges.md)


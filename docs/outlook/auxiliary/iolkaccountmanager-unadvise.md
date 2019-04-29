---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Cancela o registro de um cliente com o gerente de contas para notificações para todas as contas.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430984"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="705bc-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="705bc-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="705bc-104">Cancela o registro de um cliente com o gerente de contas para notificações para todas as contas.</span><span class="sxs-lookup"><span data-stu-id="705bc-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="705bc-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="705bc-105">Quick info</span></span>

<span data-ttu-id="705bc-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="705bc-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="705bc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="705bc-107">Parameters</span></span>

<span data-ttu-id="705bc-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="705bc-108">_dwCookie_</span></span>
  
> <span data-ttu-id="705bc-109">no O cookie retornado por [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="705bc-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="705bc-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="705bc-110">Return values</span></span>

|<span data-ttu-id="705bc-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="705bc-111">**HRESULT**</span></span>|<span data-ttu-id="705bc-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="705bc-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="705bc-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="705bc-113">S_OK</span></span>  <br/> |<span data-ttu-id="705bc-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="705bc-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="705bc-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="705bc-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="705bc-116">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="705bc-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="705bc-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="705bc-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="705bc-118">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="705bc-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="705bc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="705bc-119">See also</span></span>

- [<span data-ttu-id="705bc-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="705bc-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="705bc-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="705bc-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)


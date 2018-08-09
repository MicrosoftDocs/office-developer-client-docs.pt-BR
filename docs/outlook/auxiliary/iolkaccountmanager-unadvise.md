---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Cancela o registro de um cliente com o Gerenciador de contas para notificações para todas as contas.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765970"
---
# <a name="iolkaccountmanagerunadvise"></a><span data-ttu-id="74d25-103">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="74d25-103">IOlkAccountManager::Unadvise</span></span>

<span data-ttu-id="74d25-104">Cancela o registro de um cliente com o Gerenciador de contas para notificações para todas as contas.</span><span class="sxs-lookup"><span data-stu-id="74d25-104">Unregisters a client with the account manager for notifications for all accounts.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="74d25-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="74d25-105">Quick info</span></span>

<span data-ttu-id="74d25-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="74d25-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a><span data-ttu-id="74d25-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74d25-107">Parameters</span></span>

<span data-ttu-id="74d25-108">_dwCookie_</span><span class="sxs-lookup"><span data-stu-id="74d25-108">_dwCookie_</span></span>
  
> <span data-ttu-id="74d25-109">[in] O cookie retornado por [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span><span class="sxs-lookup"><span data-stu-id="74d25-109">[in] The cookie returned by [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).</span></span>
    
## <a name="return-values"></a><span data-ttu-id="74d25-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="74d25-110">Return values</span></span>

|<span data-ttu-id="74d25-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74d25-111">**HRESULT**</span></span>|<span data-ttu-id="74d25-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="74d25-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="74d25-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="74d25-113">S_OK</span></span>  <br/> |<span data-ttu-id="74d25-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="74d25-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="74d25-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="74d25-115">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="74d25-116">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="74d25-116">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="74d25-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="74d25-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="74d25-118">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="74d25-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74d25-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="74d25-119">See also</span></span>

- [<span data-ttu-id="74d25-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="74d25-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="74d25-121">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="74d25-121">IOlkAccountManager::Advise</span></span>](iolkaccountmanager-advise.md)


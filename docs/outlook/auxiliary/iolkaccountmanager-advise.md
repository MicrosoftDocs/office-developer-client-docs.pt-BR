---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra um cliente com o gerenciador de contas para notificações sobre todas as contas.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427707"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="46a7e-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="46a7e-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="46a7e-104">Registra um cliente com o gerenciador de contas para notificações sobre todas as contas.</span><span class="sxs-lookup"><span data-stu-id="46a7e-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="46a7e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="46a7e-105">Quick info</span></span>

<span data-ttu-id="46a7e-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="46a7e-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="46a7e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46a7e-107">Parameters</span></span>

<span data-ttu-id="46a7e-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="46a7e-108">_pNotify_</span></span>
  
> <span data-ttu-id="46a7e-109">[in] Uma interface [IOlkAccountNotify](iolkaccountnotify.md) que o gerente de conta usará para enviar notificações ao cliente.</span><span class="sxs-lookup"><span data-stu-id="46a7e-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="46a7e-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="46a7e-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="46a7e-111">[out] Um cookie que [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) usará ao remover o registro da conta.</span><span class="sxs-lookup"><span data-stu-id="46a7e-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="46a7e-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="46a7e-112">Return values</span></span>

|<span data-ttu-id="46a7e-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46a7e-113">**HRESULT**</span></span>|<span data-ttu-id="46a7e-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="46a7e-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46a7e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="46a7e-115">S_OK</span></span>  <br/> |<span data-ttu-id="46a7e-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="46a7e-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="46a7e-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="46a7e-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="46a7e-118">Um argumento inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="46a7e-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="46a7e-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="46a7e-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="46a7e-120">O gerenciador de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="46a7e-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46a7e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="46a7e-121">See also</span></span>

- [<span data-ttu-id="46a7e-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="46a7e-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="46a7e-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="46a7e-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)


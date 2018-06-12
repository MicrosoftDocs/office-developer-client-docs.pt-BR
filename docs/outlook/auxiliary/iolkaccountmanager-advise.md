---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra um cliente com o Gerenciador de contas para notificações sobre todas as contas.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765954"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="f19e2-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="f19e2-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="f19e2-104">Registra um cliente com o Gerenciador de contas para notificações sobre todas as contas.</span><span class="sxs-lookup"><span data-stu-id="f19e2-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f19e2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f19e2-105">Quick info</span></span>

<span data-ttu-id="f19e2-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f19e2-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="f19e2-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f19e2-107">Parameters</span></span>

<span data-ttu-id="f19e2-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="f19e2-108">_pNotify_</span></span>
  
> <span data-ttu-id="f19e2-109">[in] Uma interface [IOlkAccountNotify](iolkaccountnotify.md) que o gerente de conta será usado para enviar notificações para o cliente.</span><span class="sxs-lookup"><span data-stu-id="f19e2-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="f19e2-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="f19e2-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="f19e2-111">[out] Um cookie que [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) usará ao remover o registro para a conta.</span><span class="sxs-lookup"><span data-stu-id="f19e2-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f19e2-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f19e2-112">Return values</span></span>

|<span data-ttu-id="f19e2-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f19e2-113">**HRESULT**</span></span>|<span data-ttu-id="f19e2-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f19e2-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f19e2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f19e2-115">S_OK</span></span>  <br/> |<span data-ttu-id="f19e2-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f19e2-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="f19e2-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f19e2-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f19e2-118">Um argumento inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="f19e2-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="f19e2-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f19e2-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f19e2-120">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="f19e2-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f19e2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f19e2-121">See also</span></span>

- [<span data-ttu-id="f19e2-122">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="f19e2-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="f19e2-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="f19e2-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)


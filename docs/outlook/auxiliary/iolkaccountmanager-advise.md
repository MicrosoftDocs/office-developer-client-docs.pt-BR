---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Registra um cliente com o gerente de contas para notificações sobre todas as contas.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322194"
---
# <a name="iolkaccountmanageradvise"></a><span data-ttu-id="fec71-103">IOlkAccountManager::Advise</span><span class="sxs-lookup"><span data-stu-id="fec71-103">IOlkAccountManager::Advise</span></span>

<span data-ttu-id="fec71-104">Registra um cliente com o gerente de contas para notificações sobre todas as contas.</span><span class="sxs-lookup"><span data-stu-id="fec71-104">Registers a client with the account manager for notifications regarding all accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fec71-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fec71-105">Quick info</span></span>

<span data-ttu-id="fec71-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="fec71-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a><span data-ttu-id="fec71-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fec71-107">Parameters</span></span>

<span data-ttu-id="fec71-108">_pNotify_</span><span class="sxs-lookup"><span data-stu-id="fec71-108">_pNotify_</span></span>
  
> <span data-ttu-id="fec71-109">no Uma interface [IOlkAccountNotify](iolkaccountnotify.md) que o gerente de contas usará para enviar notificações ao cliente.</span><span class="sxs-lookup"><span data-stu-id="fec71-109">[in] An [IOlkAccountNotify](iolkaccountnotify.md) interface that the account manager will use to send notifications to the client.</span></span> 
    
<span data-ttu-id="fec71-110">_pdwCookie_</span><span class="sxs-lookup"><span data-stu-id="fec71-110">_pdwCookie_</span></span>
  
> <span data-ttu-id="fec71-111">bota Um cookie que [IOlkAccountManager:: Unadvise](iolkaccountmanager-unadvise.md) será usado ao remover o registro da conta.</span><span class="sxs-lookup"><span data-stu-id="fec71-111">[out] A cookie that [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) will use when removing the registration for the account.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fec71-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fec71-112">Return values</span></span>

|<span data-ttu-id="fec71-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fec71-113">**HRESULT**</span></span>|<span data-ttu-id="fec71-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fec71-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec71-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="fec71-115">S_OK</span></span>  <br/> |<span data-ttu-id="fec71-116">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fec71-116">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="fec71-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fec71-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="fec71-118">Um argumento inválido foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="fec71-118">An invalid argument has been provided.</span></span>  <br/> |
|<span data-ttu-id="fec71-119">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="fec71-119">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="fec71-120">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="fec71-120">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fec71-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec71-121">See also</span></span>

- [<span data-ttu-id="fec71-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="fec71-122">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fec71-123">IOlkAccountManager::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fec71-123">IOlkAccountManager::Unadvise</span></span>](iolkaccountmanager-unadvise.md)


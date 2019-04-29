---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Notifica o cliente sobre as alterações na conta especificada.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424564"
---
# <a name="iolkaccountnotifynotify"></a><span data-ttu-id="fc060-103">IOlkAccountNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="fc060-103">IOlkAccountNotify::Notify</span></span>

<span data-ttu-id="fc060-104">Notifica o cliente sobre as alterações na conta especificada.</span><span class="sxs-lookup"><span data-stu-id="fc060-104">Notifies the client of changes to the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc060-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fc060-105">Quick info</span></span>

<span data-ttu-id="fc060-106">Consulte [IOlkAccountNotify](iolkaccountnotify.md).</span><span class="sxs-lookup"><span data-stu-id="fc060-106">See [IOlkAccountNotify](iolkaccountnotify.md).</span></span>
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="fc060-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc060-107">Parameters</span></span>

<span data-ttu-id="fc060-108">_dwNotify_</span><span class="sxs-lookup"><span data-stu-id="fc060-108">_dwNotify_</span></span>
  
> <span data-ttu-id="fc060-109">no O tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="fc060-109">[in] The type of notification.</span></span> <span data-ttu-id="fc060-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="fc060-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="fc060-111">NOTIFY_ACCT_CHANGED</span><span class="sxs-lookup"><span data-stu-id="fc060-111">NOTIFY_ACCT_CHANGED</span></span> 
    
   - <span data-ttu-id="fc060-112">NOTIFY_ACCT_CREATED</span><span class="sxs-lookup"><span data-stu-id="fc060-112">NOTIFY_ACCT_CREATED</span></span> 
    
   - <span data-ttu-id="fc060-113">NOTIFY_ACCT_DELETED</span><span class="sxs-lookup"><span data-stu-id="fc060-113">NOTIFY_ACCT_DELETED</span></span>
    
   - <span data-ttu-id="fc060-114">NOTIFY_ACCT_ORDER_CHANGED</span><span class="sxs-lookup"><span data-stu-id="fc060-114">NOTIFY_ACCT_ORDER_CHANGED</span></span> 
    
   - <span data-ttu-id="fc060-115">NOTIFY_ACCT_PREDELETED</span><span class="sxs-lookup"><span data-stu-id="fc060-115">NOTIFY_ACCT_PREDELETED</span></span> 
    
 <span data-ttu-id="fc060-116">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="fc060-116">_dwAcctID_</span></span>
  
> <span data-ttu-id="fc060-117">no A ID da conta que foi criada, alterada, excluída ou excluída.</span><span class="sxs-lookup"><span data-stu-id="fc060-117">[in] The account ID of the account that has been created, changed, deleted, or pre-deleted.</span></span>
    
 <span data-ttu-id="fc060-118">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fc060-118">_dwFlags_</span></span>
  
>  <span data-ttu-id="fc060-119">no Não usado.</span><span class="sxs-lookup"><span data-stu-id="fc060-119">[in] Not used.</span></span> <span data-ttu-id="fc060-120">OLK_ACCOUNT_NO_FLAGS é o único valor com suporte.</span><span class="sxs-lookup"><span data-stu-id="fc060-120">OLK_ACCOUNT_NO_FLAGS is the only supported value.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fc060-121">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fc060-121">Return values</span></span>

<span data-ttu-id="fc060-122">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="fc060-122">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc060-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc060-123">See also</span></span>

- [<span data-ttu-id="fc060-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="fc060-124">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="fc060-125">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="fc060-125">IOlkAccountManager</span></span>](iolkaccountmanager.md)


---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Exclui a conta especificada.
ms.openlocfilehash: 1c0b246af10dac1af9c61f368d082a92c7b3616a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765962"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="f5fe5-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="f5fe5-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="f5fe5-104">Exclui a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="f5fe5-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5fe5-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f5fe5-105">Quick info</span></span>

<span data-ttu-id="f5fe5-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="f5fe5-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="f5fe5-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f5fe5-107">Parameters</span></span>

<span data-ttu-id="f5fe5-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="f5fe5-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="f5fe5-109">[in] A ID de conta da conta a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f5fe5-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="f5fe5-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f5fe5-110">Return values</span></span>

|<span data-ttu-id="f5fe5-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f5fe5-111">**HRESULT**</span></span>|<span data-ttu-id="f5fe5-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5fe5-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f5fe5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5fe5-113">S_OK</span></span>  <br/> |<span data-ttu-id="f5fe5-114">A chamada foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="f5fe5-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="f5fe5-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f5fe5-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="f5fe5-116">A conta especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="f5fe5-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="f5fe5-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f5fe5-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="f5fe5-118">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="f5fe5-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5fe5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5fe5-119">See also</span></span>

- [<span data-ttu-id="f5fe5-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="f5fe5-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="f5fe5-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="f5fe5-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)


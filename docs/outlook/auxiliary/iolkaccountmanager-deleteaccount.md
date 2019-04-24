---
title: IOlkAccountManagerDeleteAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: df210364-fe20-8e33-a455-9902f04ec739
description: Exclui a conta especificada.
ms.openlocfilehash: 3e39b7b9af57f64dd124e1bf836db68664709b8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322208"
---
# <a name="iolkaccountmanagerdeleteaccount"></a><span data-ttu-id="7403f-103">IOlkAccountManager::DeleteAccount</span><span class="sxs-lookup"><span data-stu-id="7403f-103">IOlkAccountManager::DeleteAccount</span></span>

<span data-ttu-id="7403f-104">Exclui a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="7403f-104">Deletes the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7403f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7403f-105">Quick info</span></span>

<span data-ttu-id="7403f-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7403f-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DeleteAccount (  
    DWORD dwAcctID, 
);
```

## <a name="parameters"></a><span data-ttu-id="7403f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7403f-107">Parameters</span></span>

<span data-ttu-id="7403f-108">_dwAcctID_</span><span class="sxs-lookup"><span data-stu-id="7403f-108">_dwAcctID_</span></span>
  
> <span data-ttu-id="7403f-109">no A ID da conta a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="7403f-109">[in] The account ID of the account to be deleted.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7403f-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7403f-110">Return values</span></span>

|<span data-ttu-id="7403f-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7403f-111">**HRESULT**</span></span>|<span data-ttu-id="7403f-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7403f-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7403f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7403f-113">S_OK</span></span>  <br/> |<span data-ttu-id="7403f-114">A chamada teve êxito</span><span class="sxs-lookup"><span data-stu-id="7403f-114">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="7403f-115">E_ACCT_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7403f-115">E_ACCT_NOT_FOUND</span></span>  <br/> |<span data-ttu-id="7403f-116">A conta especificada não pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="7403f-116">The specified account cannot be found.</span></span>  <br/> |
|<span data-ttu-id="7403f-117">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7403f-117">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7403f-118">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="7403f-118">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7403f-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="7403f-119">See also</span></span>

- [<span data-ttu-id="7403f-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="7403f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="7403f-121">IOlkAccountManager::FindAccount</span><span class="sxs-lookup"><span data-stu-id="7403f-121">IOlkAccountManager::FindAccount</span></span>](iolkaccountmanager-findaccount.md)


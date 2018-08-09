---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa o gerente de conta para uso.
ms.openlocfilehash: 621c6a73ab2bcbdff17b87ce15af8b4e0c2e1e24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765958"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="65380-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="65380-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="65380-104">Inicializa o gerente de conta para uso.</span><span class="sxs-lookup"><span data-stu-id="65380-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="65380-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="65380-105">Quick info</span></span>

<span data-ttu-id="65380-106">Consulte [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="65380-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="65380-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65380-107">Parameters</span></span>

<span data-ttu-id="65380-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="65380-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="65380-109">[in] Uma interface [IOlkAccountHelper](iolkaccounthelper.md) que fornece a funcionalidade de auxiliar de conta.</span><span class="sxs-lookup"><span data-stu-id="65380-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="65380-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="65380-110">_dwFlags_</span></span>
  
> <span data-ttu-id="65380-111">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="65380-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="65380-112">**ACCT_INIT_NO_STORES_CHECK** — evita a sincronização com um repositório associado de uma conta (por exemplo, uma conta IMAP).</span><span class="sxs-lookup"><span data-stu-id="65380-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="65380-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** — serviços MAPI impede da sincronização com contas.</span><span class="sxs-lookup"><span data-stu-id="65380-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
    
   - <span data-ttu-id="65380-114">**OLK_ACCOUNT_NO_FLAGS** — serviços MAPI sincroniza com contas.</span><span class="sxs-lookup"><span data-stu-id="65380-114">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="65380-115">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="65380-115">Return values</span></span>

|<span data-ttu-id="65380-116">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65380-116">**HRESULT**</span></span>|<span data-ttu-id="65380-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="65380-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="65380-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="65380-118">S_OK</span></span>  <br/> |<span data-ttu-id="65380-119">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="65380-119">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="65380-120">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="65380-120">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="65380-121">**Inicialização** já foi chamado.</span><span class="sxs-lookup"><span data-stu-id="65380-121">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="65380-122">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="65380-122">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="65380-123">O gerente de conta não foi possível acessar as configurações do registro necessárias.</span><span class="sxs-lookup"><span data-stu-id="65380-123">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65380-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="65380-124">Remarks</span></span>

<span data-ttu-id="65380-125">O cliente deve chamar **IOlkAccountManager::Init** para inicializar a conta do gerente antes de usar o Gerenciador de conta para contas de acessar ou configurar as notificações.</span><span class="sxs-lookup"><span data-stu-id="65380-125">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="65380-126">Como o Outlook sincroniza automaticamente serviços MAPI com contas na inicialização, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** , a menos que haja uma causa específica para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="65380-126">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65380-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="65380-127">See also</span></span>

- [<span data-ttu-id="65380-128">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="65380-128">Constants (Account management API)</span></span>](constants-account-management-api.md)


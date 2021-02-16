---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: Inicializa o gerente de conta para uso.
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322033"
---
# <a name="iolkaccountmanagerinit"></a><span data-ttu-id="fa6a0-103">IOlkAccountManager::Init</span><span class="sxs-lookup"><span data-stu-id="fa6a0-103">IOlkAccountManager::Init</span></span>

<span data-ttu-id="fa6a0-104">Inicializa o gerente de conta para uso.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-104">Initializes the account manager for use.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fa6a0-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="fa6a0-105">Quick info</span></span>

<span data-ttu-id="fa6a0-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="fa6a0-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a><span data-ttu-id="fa6a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa6a0-107">Parameters</span></span>

<span data-ttu-id="fa6a0-108">_pAcctHelper_</span><span class="sxs-lookup"><span data-stu-id="fa6a0-108">_pAcctHelper_</span></span>
  
> <span data-ttu-id="fa6a0-109">[em] Uma interface [IOlkAccountHelper](iolkaccounthelper.md)que fornece a funcionalidade de ajuda da conta.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-109">[in] An [IOlkAccountHelper](iolkaccounthelper.md) interface that provides account helper functionality.</span></span> 
    
<span data-ttu-id="fa6a0-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fa6a0-110">_dwFlags_</span></span>
  
> <span data-ttu-id="fa6a0-111">[in] Sinalizadores para modificar o comportamento.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-111">[in] Flags to modify behavior.</span></span>
    
   - <span data-ttu-id="fa6a0-112">**ACCT_INIT_NO_STORES_CHECK**, impede que uma conta (como uma conta IMAP) seja sincronizada com um repositório associado.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-112">**ACCT_INIT_NO_STORES_CHECK** —Prevents an account (such as an IMAP account) from synchronizing with an associated store.</span></span> 
    
   - <span data-ttu-id="fa6a0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS**, impede que os serviços MAPI sejam sincronizados com as contas.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-113">**ACCT_INIT_NOSYNCH_MAPI_ACCTS** —Prevents MAPI services from synchronizing with accounts.</span></span> 
   
   - <span data-ttu-id="fa6a0-114">**ACCT_INIT_NO_NOTIFICATIONS**, impede que o Gerente de Contas intercepte a transmissão de mensagens destinadas a outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-114">**ACCT_INIT_NO_NOTIFICATIONS** —Prevents the Account Manager from intercepting broadcast messages intended for other applications.</span></span> 
   
   - <span data-ttu-id="fa6a0-115">**OLK_ACCOUNT_NO_FLAGS**, sincroniza os serviços MAPI com as contas.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-115">**OLK_ACCOUNT_NO_FLAGS** —Synchronizes MAPI services with accounts.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fa6a0-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fa6a0-116">Return values</span></span>

|<span data-ttu-id="fa6a0-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fa6a0-117">**HRESULT**</span></span>|<span data-ttu-id="fa6a0-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fa6a0-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa6a0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa6a0-119">S_OK</span></span>  <br/> |<span data-ttu-id="fa6a0-120">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-120">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="fa6a0-121">E_OLK_ALREADY_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="fa6a0-121">E_OLK_ALREADY_INITIALIZED</span></span>  <br/> |<span data-ttu-id="fa6a0-122">**Init** já foi chamado.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-122">**Init** has already been called.</span></span>  <br/> |
|<span data-ttu-id="fa6a0-123">E_OLK_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="fa6a0-123">E_OLK_REGISTRY</span></span>  <br/> |<span data-ttu-id="fa6a0-124">O gerente de conta não pôde acessar as configurações de registro necessárias.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-124">The account manager could not access the required registry settings.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa6a0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa6a0-125">Remarks</span></span>

<span data-ttu-id="fa6a0-126">O cliente deverá ligar **IOlkAccountManager::Init** para inicializar o gerente de conta antes de usar o gerenciador de conta para acessar contas ou configurar notificações.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-126">The client must call **IOlkAccountManager::Init** to initialize the account manager before using the account manager to access accounts or set up notifications.</span></span> <span data-ttu-id="fa6a0-127">Como o Outlook sincroniza automaticamente serviços MAPI com contas na inicialização, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** a menos que haja uma causa específica para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="fa6a0-127">Because Outlook automatically synchronizes MAPI services with accounts on startup, use **ACCT_INIT_NOSYNCH_MAPI_ACCTS** unless there is a specific cause to synchronize.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa6a0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa6a0-128">See also</span></span>

- [<span data-ttu-id="fa6a0-129">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="fa6a0-129">Constants (Account management API)</span></span>](constants-account-management-api.md)


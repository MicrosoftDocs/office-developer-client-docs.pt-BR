---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtém a ordem da categoria de contas especificada.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424620"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="c7457-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="c7457-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="c7457-104">Obtém a ordem da categoria de contas especificada.</span><span class="sxs-lookup"><span data-stu-id="c7457-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c7457-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c7457-105">Quick info</span></span>

<span data-ttu-id="c7457-106">Consulte [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="c7457-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="c7457-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7457-107">Parameters</span></span>

<span data-ttu-id="c7457-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="c7457-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="c7457-109">[in] A ID de classe de categoria para a qual obter o pedido.</span><span class="sxs-lookup"><span data-stu-id="c7457-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="c7457-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c7457-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="c7457-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="c7457-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="c7457-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="c7457-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="c7457-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="c7457-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="c7457-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="c7457-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="c7457-115">[out] O número de contas.</span><span class="sxs-lookup"><span data-stu-id="c7457-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="c7457-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="c7457-116">_prgAccts_</span></span>
  
> <span data-ttu-id="c7457-117">[out] Um ponteiro para uma matriz de contas.</span><span class="sxs-lookup"><span data-stu-id="c7457-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="c7457-118">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c7457-118">Return values</span></span>

|<span data-ttu-id="c7457-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c7457-119">**HRESULT**</span></span>|<span data-ttu-id="c7457-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c7457-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7457-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7457-121">S_OK</span></span>  <br/> |<span data-ttu-id="c7457-122">A chamada foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="c7457-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="c7457-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c7457-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="c7457-124">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="c7457-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="c7457-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="c7457-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="c7457-126">O gerenciador de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="c7457-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7457-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7457-127">Remarks</span></span>

<span data-ttu-id="c7457-128">Antes de chamar esse método, o chamador aloca apenas um ponteiro de matriz  *prgAccts,*  mas nenhuma memória para a matriz na qual  *prgAccts*  aponta.</span><span class="sxs-lookup"><span data-stu-id="c7457-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="c7457-129">Depois que esse método retorna, o chamador deve usar [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) para liberar a memória alocada para  *prgAccts*  .</span><span class="sxs-lookup"><span data-stu-id="c7457-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7457-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7457-130">See also</span></span>

- [<span data-ttu-id="c7457-131">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="c7457-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="c7457-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="c7457-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)


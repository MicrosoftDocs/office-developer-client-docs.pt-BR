---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtém a ordenação da categoria de contas especificada.
ms.openlocfilehash: 3eb6dd96caa43f81eba86a389c938ef90c9533b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322026"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="aa5d6-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="aa5d6-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="aa5d6-104">Obtém a ordenação da categoria de contas especificada.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aa5d6-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aa5d6-105">Quick info</span></span>

<span data-ttu-id="aa5d6-106">Consulte [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="aa5d6-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="aa5d6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa5d6-107">Parameters</span></span>

<span data-ttu-id="aa5d6-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="aa5d6-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="aa5d6-109">no A ID de classe de categoria para a qual obter o pedido.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="aa5d6-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="aa5d6-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="aa5d6-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="aa5d6-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="aa5d6-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="aa5d6-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="aa5d6-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="aa5d6-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="aa5d6-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="aa5d6-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="aa5d6-115">bota O número de contas.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="aa5d6-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="aa5d6-116">_prgAccts_</span></span>
  
> <span data-ttu-id="aa5d6-117">bota Um ponteiro para uma matriz de contas.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="aa5d6-118">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aa5d6-118">Return values</span></span>

|<span data-ttu-id="aa5d6-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="aa5d6-119">**HRESULT**</span></span>|<span data-ttu-id="aa5d6-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aa5d6-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa5d6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa5d6-121">S_OK</span></span>  <br/> |<span data-ttu-id="aa5d6-122">A chamada teve êxito</span><span class="sxs-lookup"><span data-stu-id="aa5d6-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="aa5d6-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="aa5d6-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="aa5d6-124">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="aa5d6-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="aa5d6-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="aa5d6-126">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa5d6-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa5d6-127">Remarks</span></span>

<span data-ttu-id="aa5d6-128">Antes de chamar esse método, o chamador aloca apenas um ponteiro de matriz *prgAccts* , mas não há memória para a matriz na qual *prgAccts* aponta.</span><span class="sxs-lookup"><span data-stu-id="aa5d6-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="aa5d6-129">Após o método retornar, o chamador deverá usar [IOlkAccountManager:: freememory](iolkaccountmanager-freememory.md) para liberar a memória alocada para o *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="aa5d6-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa5d6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa5d6-130">See also</span></span>

- [<span data-ttu-id="aa5d6-131">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="aa5d6-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="aa5d6-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="aa5d6-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)


---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: Obtém a ordenação da categoria especificada das contas.
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765968"
---
# <a name="iolkaccountmanagergetorder"></a><span data-ttu-id="909f7-103">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="909f7-103">IOlkAccountManager::GetOrder</span></span>

<span data-ttu-id="909f7-104">Obtém a ordenação da categoria especificada das contas.</span><span class="sxs-lookup"><span data-stu-id="909f7-104">Gets the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="909f7-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="909f7-105">Quick info</span></span>

<span data-ttu-id="909f7-106">Consulte [IOlkAccountManager](iolkaccountmanager.md)</span><span class="sxs-lookup"><span data-stu-id="909f7-106">See [IOlkAccountManager](iolkaccountmanager.md)</span></span>
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a><span data-ttu-id="909f7-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="909f7-107">Parameters</span></span>

<span data-ttu-id="909f7-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="909f7-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="909f7-109">[in] A ID de classe de categoria para o qual deseja obter a ordem.</span><span class="sxs-lookup"><span data-stu-id="909f7-109">[in] The category class ID for which to get the order.</span></span> <span data-ttu-id="909f7-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="909f7-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="909f7-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="909f7-111">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="909f7-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="909f7-112">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="909f7-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="909f7-113">CLSID_OlkStore</span></span>
    
<span data-ttu-id="909f7-114">_pcAccts_</span><span class="sxs-lookup"><span data-stu-id="909f7-114">_pcAccts_</span></span>
  
>  <span data-ttu-id="909f7-115">[out] O número de contas.</span><span class="sxs-lookup"><span data-stu-id="909f7-115">[out] The number of accounts.</span></span> 
    
<span data-ttu-id="909f7-116">_prgAccts_</span><span class="sxs-lookup"><span data-stu-id="909f7-116">_prgAccts_</span></span>
  
> <span data-ttu-id="909f7-117">[out] Um ponteiro para uma matriz de contas.</span><span class="sxs-lookup"><span data-stu-id="909f7-117">[out] A pointer to an array of accounts.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="909f7-118">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="909f7-118">Return values</span></span>

|<span data-ttu-id="909f7-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="909f7-119">**HRESULT**</span></span>|<span data-ttu-id="909f7-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="909f7-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="909f7-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="909f7-121">S_OK</span></span>  <br/> |<span data-ttu-id="909f7-122">A chamada foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="909f7-122">The call succeeded</span></span>  <br/> |
|<span data-ttu-id="909f7-123">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="909f7-123">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="909f7-124">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="909f7-124">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="909f7-125">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="909f7-125">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="909f7-126">O gerente de conta não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="909f7-126">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="909f7-127">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="909f7-127">Remarks</span></span>

<span data-ttu-id="909f7-128">Antes de chamar este método, o chamador aloca apenas uma matriz ponteiro *prgAccts* , mas não há memória para a matriz nos quais pontos *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="909f7-128">Before calling this method, the caller allocates only an array pointer  *prgAccts*  but no memory for the array at which  *prgAccts*  points.</span></span> <span data-ttu-id="909f7-129">Depois que esse método retorna, o chamador deve usar [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) para liberar a memória alocada para *prgAccts* .</span><span class="sxs-lookup"><span data-stu-id="909f7-129">After this method returns, the caller must use [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) to release the memory allocated for  *prgAccts*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="909f7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="909f7-130">See also</span></span>

- [<span data-ttu-id="909f7-131">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="909f7-131">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="909f7-132">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="909f7-132">IOlkAccountManager::SetOrder</span></span>](iolkaccountmanager-setorder.md)


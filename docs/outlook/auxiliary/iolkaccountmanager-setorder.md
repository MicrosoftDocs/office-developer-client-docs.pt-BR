---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: Modifica a ordenação da categoria especificada de contas.
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322040"
---
# <a name="iolkaccountmanagersetorder"></a><span data-ttu-id="b1806-103">IOlkAccountManager::SetOrder</span><span class="sxs-lookup"><span data-stu-id="b1806-103">IOlkAccountManager::SetOrder</span></span>

<span data-ttu-id="b1806-104">Modifica a ordenação da categoria especificada de contas.</span><span class="sxs-lookup"><span data-stu-id="b1806-104">Modifies the ordering of the specified category of accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b1806-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="b1806-105">Quick info</span></span>

<span data-ttu-id="b1806-106">Confira [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="b1806-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a><span data-ttu-id="b1806-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1806-107">Parameters</span></span>

<span data-ttu-id="b1806-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="b1806-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="b1806-109">no A ID de classe de categoria para a qual definir a ordem.</span><span class="sxs-lookup"><span data-stu-id="b1806-109">[in] The category class ID for which to set the order.</span></span> <span data-ttu-id="b1806-110">O valor deve ser uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="b1806-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="b1806-111">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="b1806-111">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="b1806-112">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="b1806-112">CLSID_OlkStore</span></span>
    
<span data-ttu-id="b1806-113">_cAccts_</span><span class="sxs-lookup"><span data-stu-id="b1806-113">_cAccts_</span></span>
  
> <span data-ttu-id="b1806-114">no O número de contas.</span><span class="sxs-lookup"><span data-stu-id="b1806-114">[in] The number of accounts.</span></span>
    
<span data-ttu-id="b1806-115">_rgAccts_</span><span class="sxs-lookup"><span data-stu-id="b1806-115">_rgAccts_</span></span>
  
> <span data-ttu-id="b1806-116">no Uma matriz de IDs de conta.</span><span class="sxs-lookup"><span data-stu-id="b1806-116">[in] An array of account IDs.</span></span> <span data-ttu-id="b1806-117">O tamanho da matriz é _cAccts_.</span><span class="sxs-lookup"><span data-stu-id="b1806-117">The size of the array is  _cAccts_.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b1806-118">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="b1806-118">Return values</span></span>

|<span data-ttu-id="b1806-119">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b1806-119">**HRESULT**</span></span>|<span data-ttu-id="b1806-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b1806-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1806-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1806-121">S_OK</span></span>  <br/> |<span data-ttu-id="b1806-122">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b1806-122">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="b1806-123">E_ACCT_WRONG_SORT_ORDER</span><span class="sxs-lookup"><span data-stu-id="b1806-123">E_ACCT_WRONG_SORT_ORDER</span></span>  <br/> |<span data-ttu-id="b1806-124">A nova ordem de classificação tem um número diferente de contas da ordem de classificação antiga.</span><span class="sxs-lookup"><span data-stu-id="b1806-124">The new sort order has a different number of accounts than the old sort order.</span></span>  <br/> |
|<span data-ttu-id="b1806-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b1806-125">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="b1806-126">Um ou mais argumentos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="b1806-126">One or more arguments are invalid.</span></span>  <br/> |
|<span data-ttu-id="b1806-127">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="b1806-127">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="b1806-128">O gerente de contas não foi inicializado para uso.</span><span class="sxs-lookup"><span data-stu-id="b1806-128">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1806-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1806-129">Remarks</span></span>

<span data-ttu-id="b1806-130">O chamador aloca memória para o ponteiro de matriz _prgAccts_ , bem como para a matriz na qual _prgAccts_ aponta.</span><span class="sxs-lookup"><span data-stu-id="b1806-130">The caller allocates memory for the array pointer  _prgAccts_ as well as for the array at which  _prgAccts_ points.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b1806-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1806-131">See also</span></span>

- [<span data-ttu-id="b1806-132">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="b1806-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="b1806-133">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="b1806-133">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)


---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Define o valor da propriedade conta especificada.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765925"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="ab42c-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="ab42c-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="ab42c-104">Define o valor da propriedade conta especificada.</span><span class="sxs-lookup"><span data-stu-id="ab42c-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ab42c-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ab42c-105">Quick info</span></span>

<span data-ttu-id="ab42c-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ab42c-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="ab42c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab42c-107">Parameters</span></span>

<span data-ttu-id="ab42c-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="ab42c-108">_dwProp_</span></span>
  
> <span data-ttu-id="ab42c-109">[in] A marca de propriedade da propriedade conta para definir.</span><span class="sxs-lookup"><span data-stu-id="ab42c-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="ab42c-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="ab42c-110">_pVar_</span></span>
  
> <span data-ttu-id="ab42c-111">[in] O valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="ab42c-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ab42c-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ab42c-112">Return values</span></span>

|<span data-ttu-id="ab42c-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab42c-113">**HRESULT**</span></span>|<span data-ttu-id="ab42c-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ab42c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab42c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab42c-115">S_OK</span></span>  <br/> |<span data-ttu-id="ab42c-116">A chamada do método foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ab42c-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="ab42c-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ab42c-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="ab42c-118">Uma marca de propriedade inválido foi especificada.</span><span class="sxs-lookup"><span data-stu-id="ab42c-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab42c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab42c-119">Remarks</span></span>

<span data-ttu-id="ab42c-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para salvar as alterações para o valor das propriedades de conta.</span><span class="sxs-lookup"><span data-stu-id="ab42c-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab42c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab42c-121">See also</span></span>

- [<span data-ttu-id="ab42c-122">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="ab42c-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="ab42c-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="ab42c-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)


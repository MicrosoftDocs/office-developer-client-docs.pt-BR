---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Define o valor da propriedade de conta especificada.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322250"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="7130f-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="7130f-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="7130f-104">Define o valor da propriedade de conta especificada.</span><span class="sxs-lookup"><span data-stu-id="7130f-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7130f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7130f-105">Quick info</span></span>

<span data-ttu-id="7130f-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="7130f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="7130f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7130f-107">Parameters</span></span>

<span data-ttu-id="7130f-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="7130f-108">_dwProp_</span></span>
  
> <span data-ttu-id="7130f-109">no A marca de propriedade da propriedade Account a ser definida.</span><span class="sxs-lookup"><span data-stu-id="7130f-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="7130f-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="7130f-110">_pVar_</span></span>
  
> <span data-ttu-id="7130f-111">no O valor da propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="7130f-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7130f-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7130f-112">Return values</span></span>

|<span data-ttu-id="7130f-113">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7130f-113">**HRESULT**</span></span>|<span data-ttu-id="7130f-114">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7130f-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7130f-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="7130f-115">S_OK</span></span>  <br/> |<span data-ttu-id="7130f-116">A chamada do método foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7130f-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="7130f-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7130f-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="7130f-118">Uma marca de propriedade inválida foi especificada.</span><span class="sxs-lookup"><span data-stu-id="7130f-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7130f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7130f-119">Remarks</span></span>

<span data-ttu-id="7130f-120">Use [IOlkAccount:: SaveChanges](iolkaccount-savechanges.md) para salvar alterações no valor das propriedades da conta.</span><span class="sxs-lookup"><span data-stu-id="7130f-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7130f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7130f-121">See also</span></span>

- [<span data-ttu-id="7130f-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="7130f-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="7130f-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="7130f-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)


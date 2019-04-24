---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtém a próxima conta no enumerador.
ms.openlocfilehash: e2ad98f7d7e71bd91d48b3824423e305baab429a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321893"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="89b3c-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="89b3c-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="89b3c-104">Obtém a próxima conta no enumerador.</span><span class="sxs-lookup"><span data-stu-id="89b3c-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89b3c-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="89b3c-105">Quick info</span></span>

<span data-ttu-id="89b3c-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="89b3c-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="89b3c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89b3c-107">Parameters</span></span>

<span data-ttu-id="89b3c-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="89b3c-108">_ppunk_</span></span>
  
> <span data-ttu-id="89b3c-109">no Um ponteiro para uma interface **IUnknown** que o cliente pode consultar para obter uma interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="89b3c-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="89b3c-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="89b3c-110">Return values</span></span>

|<span data-ttu-id="89b3c-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89b3c-111">**HRESULT**</span></span>|<span data-ttu-id="89b3c-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="89b3c-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89b3c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="89b3c-113">S_OK</span></span>  <br/> |<span data-ttu-id="89b3c-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="89b3c-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="89b3c-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="89b3c-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="89b3c-116">O enumerador atingiu o fim.</span><span class="sxs-lookup"><span data-stu-id="89b3c-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89b3c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89b3c-117">Remarks</span></span>

<span data-ttu-id="89b3c-118">A interface especificada por *ppunk* herda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="89b3c-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="89b3c-119">O cliente pode consultar esta interface (usando **IUnknown:: QueryInterface**) para obter um ponteiro para uma interface **IOlkAccount** e obter ou definir informações para essa conta.</span><span class="sxs-lookup"><span data-stu-id="89b3c-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89b3c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="89b3c-120">See also</span></span>

- [<span data-ttu-id="89b3c-121">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="89b3c-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="89b3c-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="89b3c-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="89b3c-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="89b3c-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="89b3c-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="89b3c-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)


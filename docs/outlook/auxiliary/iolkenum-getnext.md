---
title: IOlkEnumGetNext
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b387f896-c213-fc07-a12a-33917e620837
description: Obtém a próxima conta no enumerador.
ms.openlocfilehash: 496a4d787916d051c051b3a19a7113d9d50c6fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765999"
---
# <a name="iolkenumgetnext"></a><span data-ttu-id="1ef3e-103">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="1ef3e-103">IOlkEnum::GetNext</span></span>

<span data-ttu-id="1ef3e-104">Obtém a próxima conta no enumerador.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-104">Gets the next account in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1ef3e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1ef3e-105">Quick info</span></span>

<span data-ttu-id="1ef3e-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="1ef3e-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum:: GetNext( 
    LPUNKNOWN *ppunk 
);

```

## <a name="parameters"></a><span data-ttu-id="1ef3e-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1ef3e-107">Parameters</span></span>

<span data-ttu-id="1ef3e-108">_ppunk_</span><span class="sxs-lookup"><span data-stu-id="1ef3e-108">_ppunk_</span></span>
  
> <span data-ttu-id="1ef3e-109">[in] Um ponteiro para uma interface **IUnknown** que o cliente pode consultar para obter uma interface [IOlkAccount](iolkaccount.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef3e-109">[in] A pointer to an **IUnknown** interface that the client can query to obtain an [IOlkAccount](iolkaccount.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1ef3e-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1ef3e-110">Return values</span></span>

|<span data-ttu-id="1ef3e-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1ef3e-111">**HRESULT**</span></span>|<span data-ttu-id="1ef3e-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ef3e-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ef3e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ef3e-113">S_OK</span></span>  <br/> |<span data-ttu-id="1ef3e-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="1ef3e-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1ef3e-115">S_FALSE</span></span>  <br/> |<span data-ttu-id="1ef3e-116">O enumerador atingiu o final.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-116">The enumerator has reached the end.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ef3e-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="1ef3e-117">Remarks</span></span>

<span data-ttu-id="1ef3e-118">A interface especificada por *ppunk* herda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-118">The interface specified by  *ppunk*  inherits from **IUnknown**.</span></span> <span data-ttu-id="1ef3e-119">O cliente pode consultar a esta interface (usando **IUnknown:: QueryInterface**) para obter um ponteiro para uma interface **IOlkAccount** e obter ou definir informações para essa conta.</span><span class="sxs-lookup"><span data-stu-id="1ef3e-119">The client can query this interface (using **IUnknown::QueryInterface**) to obtain a pointer to an **IOlkAccount** interface, and get or set information for this account.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ef3e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ef3e-120">See also</span></span>

- [<span data-ttu-id="1ef3e-121">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="1ef3e-121">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="1ef3e-122">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="1ef3e-122">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md)  
- [<span data-ttu-id="1ef3e-123">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="1ef3e-123">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="1ef3e-124">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="1ef3e-124">IOlkEnum::Skip</span></span>](iolkenum-skip.md)


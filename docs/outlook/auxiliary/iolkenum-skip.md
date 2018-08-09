---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignora um número especificado de contas do enumerador.
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765978"
---
# <a name="iolkenumskip"></a><span data-ttu-id="05f47-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="05f47-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="05f47-104">Ignora um número especificado de contas do enumerador.</span><span class="sxs-lookup"><span data-stu-id="05f47-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="05f47-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="05f47-105">Quick info</span></span>

<span data-ttu-id="05f47-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="05f47-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="05f47-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05f47-107">Parameters</span></span>

<span data-ttu-id="05f47-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="05f47-108">_cSkip_</span></span>
  
> <span data-ttu-id="05f47-109">[in] O número de contas seja ignorada.</span><span class="sxs-lookup"><span data-stu-id="05f47-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="05f47-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="05f47-110">Return values</span></span>

<span data-ttu-id="05f47-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="05f47-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05f47-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="05f47-112">See also</span></span>

- [<span data-ttu-id="05f47-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="05f47-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="05f47-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="05f47-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="05f47-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="05f47-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)


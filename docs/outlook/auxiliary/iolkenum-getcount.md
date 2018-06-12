---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtém o número de contas no enumerador.
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765985"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="1fda0-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="1fda0-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="1fda0-104">Obtém o número de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="1fda0-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1fda0-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="1fda0-105">Quick info</span></span>

<span data-ttu-id="1fda0-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="1fda0-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="1fda0-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1fda0-107">Parameters</span></span>

<span data-ttu-id="1fda0-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="1fda0-108">_pulCount_</span></span>
  
> <span data-ttu-id="1fda0-109">[out] Um ponteiro para o número de objetos que está sendo enumerado.</span><span class="sxs-lookup"><span data-stu-id="1fda0-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="1fda0-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="1fda0-110">Return values</span></span>

<span data-ttu-id="1fda0-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="1fda0-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1fda0-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fda0-112">See also</span></span>

- [<span data-ttu-id="1fda0-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="1fda0-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="1fda0-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="1fda0-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="1fda0-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="1fda0-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)


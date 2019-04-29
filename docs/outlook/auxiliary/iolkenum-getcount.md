---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: Obtém o número de contas no enumerador.
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421820"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="baf06-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="baf06-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="baf06-104">Obtém o número de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="baf06-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="baf06-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="baf06-105">Quick info</span></span>

<span data-ttu-id="baf06-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="baf06-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="baf06-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="baf06-107">Parameters</span></span>

<span data-ttu-id="baf06-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="baf06-108">_pulCount_</span></span>
  
> <span data-ttu-id="baf06-109">bota Um ponteiro para o número de objetos que estão sendo enumerados.</span><span class="sxs-lookup"><span data-stu-id="baf06-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="baf06-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="baf06-110">Return values</span></span>

<span data-ttu-id="baf06-111">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="baf06-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="baf06-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="baf06-112">See also</span></span>

- [<span data-ttu-id="baf06-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="baf06-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="baf06-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="baf06-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="baf06-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="baf06-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)


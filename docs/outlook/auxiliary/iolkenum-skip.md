---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: Ignora um número especificado de contas no enumerador.
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404775"
---
# <a name="iolkenumskip"></a><span data-ttu-id="7c2f2-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="7c2f2-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="7c2f2-104">Ignora um número especificado de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="7c2f2-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7c2f2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7c2f2-105">Quick info</span></span>

<span data-ttu-id="7c2f2-106">Consulte [IOlkEnum](iolkenum.md).</span><span class="sxs-lookup"><span data-stu-id="7c2f2-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="7c2f2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c2f2-107">Parameters</span></span>

<span data-ttu-id="7c2f2-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="7c2f2-108">_cSkip_</span></span>
  
> <span data-ttu-id="7c2f2-109">[in] O número de contas a serem ignoradas.</span><span class="sxs-lookup"><span data-stu-id="7c2f2-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="7c2f2-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7c2f2-110">Return values</span></span>

<span data-ttu-id="7c2f2-111">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="7c2f2-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c2f2-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c2f2-112">See also</span></span>

- [<span data-ttu-id="7c2f2-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="7c2f2-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="7c2f2-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="7c2f2-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="7c2f2-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="7c2f2-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)


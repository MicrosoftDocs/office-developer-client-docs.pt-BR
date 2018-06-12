---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe a enumeração para um período de tempo especificado.
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765817"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="d1404-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="d1404-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="d1404-104">Restringe a enumeração para um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d1404-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d1404-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d1404-105">Quick info</span></span>

<span data-ttu-id="d1404-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="d1404-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="d1404-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="d1404-107">Parameters</span></span>

<span data-ttu-id="d1404-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="d1404-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="d1404-109">[in] A hora de início para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="d1404-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="d1404-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="d1404-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="d1404-111">[in] A hora de término para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="d1404-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d1404-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d1404-112">Return values</span></span>

<span data-ttu-id="d1404-113">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d1404-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1404-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d1404-114">Remarks</span></span>

<span data-ttu-id="d1404-115">Este método também redefine a enumeração.</span><span class="sxs-lookup"><span data-stu-id="d1404-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1404-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1404-116">See also</span></span>

- [<span data-ttu-id="d1404-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="d1404-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="d1404-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="d1404-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="d1404-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="d1404-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="d1404-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="d1404-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="d1404-121">Use o tempo relativo para acessar dados do tipo disponível/ocupado</span><span class="sxs-lookup"><span data-stu-id="d1404-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


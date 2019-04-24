---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: Restringe a enumeração para um período específico.
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317560"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="36f57-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="36f57-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="36f57-104">Restringe a enumeração para um período específico.</span><span class="sxs-lookup"><span data-stu-id="36f57-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="36f57-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="36f57-105">Quick info</span></span>

<span data-ttu-id="36f57-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="36f57-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="36f57-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36f57-107">Parameters</span></span>

<span data-ttu-id="36f57-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="36f57-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="36f57-109">no A hora de início para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="36f57-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="36f57-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="36f57-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="36f57-111">no A hora de término para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="36f57-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="36f57-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="36f57-112">Return values</span></span>

<span data-ttu-id="36f57-113">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="36f57-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36f57-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="36f57-114">Remarks</span></span>

<span data-ttu-id="36f57-115">Esse método também redefine a enumeração.</span><span class="sxs-lookup"><span data-stu-id="36f57-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36f57-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="36f57-116">See also</span></span>

- [<span data-ttu-id="36f57-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="36f57-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="36f57-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="36f57-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="36f57-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="36f57-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="36f57-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="36f57-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="36f57-121">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="36f57-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


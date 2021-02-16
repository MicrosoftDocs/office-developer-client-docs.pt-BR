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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431943"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="8d8f9-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="8d8f9-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="8d8f9-104">Restringe a enumeração para um período específico.</span><span class="sxs-lookup"><span data-stu-id="8d8f9-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8d8f9-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8d8f9-105">Quick info</span></span>

<span data-ttu-id="8d8f9-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="8d8f9-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="8d8f9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d8f9-107">Parameters</span></span>

<span data-ttu-id="8d8f9-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="8d8f9-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="8d8f9-109">[in] A hora de início para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="8d8f9-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="8d8f9-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="8d8f9-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="8d8f9-111">[in] A hora de término para restringir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="8d8f9-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8d8f9-112">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8d8f9-112">Return values</span></span>

<span data-ttu-id="8d8f9-113">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="8d8f9-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d8f9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d8f9-114">Remarks</span></span>

<span data-ttu-id="8d8f9-115">Esse método também redefine a enumeração.</span><span class="sxs-lookup"><span data-stu-id="8d8f9-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d8f9-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d8f9-116">See also</span></span>

- [<span data-ttu-id="8d8f9-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="8d8f9-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="8d8f9-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="8d8f9-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="8d8f9-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="8d8f9-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="8d8f9-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="8d8f9-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="8d8f9-121">Usar o tempo relativo para acessar dados de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="8d8f9-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)


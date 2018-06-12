---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Ignora um número especificado de blocos de informações de disponibilidade de dados.
ms.openlocfilehash: 63f699d09e143a879702e8dc76beb8a969a77b82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765819"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="72da9-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="72da9-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="72da9-104">Ignora um número especificado de blocos de informações de disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="72da9-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="72da9-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="72da9-105">Quick info</span></span>

<span data-ttu-id="72da9-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="72da9-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="72da9-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="72da9-107">Parameters</span></span>

<span data-ttu-id="72da9-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="72da9-108">_celt_</span></span>
  
>  <span data-ttu-id="72da9-109">[in] O número de blocos de livre/ocupado para ignorar.</span><span class="sxs-lookup"><span data-stu-id="72da9-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="72da9-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="72da9-110">Return values</span></span>

<span data-ttu-id="72da9-111">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="72da9-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72da9-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="72da9-112">See also</span></span>

- [<span data-ttu-id="72da9-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="72da9-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="72da9-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="72da9-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="72da9-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="72da9-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="72da9-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="72da9-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)


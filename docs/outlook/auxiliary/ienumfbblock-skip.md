---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: Pula um número específico de blocos de disponibilidade de dados.
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425719"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="88d44-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="88d44-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="88d44-104">Pula um número específico de blocos de disponibilidade de dados.</span><span class="sxs-lookup"><span data-stu-id="88d44-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="88d44-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="88d44-105">Quick info</span></span>

<span data-ttu-id="88d44-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="88d44-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="88d44-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88d44-107">Parameters</span></span>

<span data-ttu-id="88d44-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="88d44-108">_celt_</span></span>
  
>  <span data-ttu-id="88d44-109">no O número de blocos de disponibilidade a ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="88d44-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="88d44-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="88d44-110">Return values</span></span>

<span data-ttu-id="88d44-111">S_OK se a chamada foi bem-sucedida. Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="88d44-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="88d44-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="88d44-112">See also</span></span>

- [<span data-ttu-id="88d44-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="88d44-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="88d44-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="88d44-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="88d44-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="88d44-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="88d44-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="88d44-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)


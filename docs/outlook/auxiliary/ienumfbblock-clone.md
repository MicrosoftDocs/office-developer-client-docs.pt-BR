---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definir o cursor para o início do enumerador.
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765820"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="18001-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="18001-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="18001-104">Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definir o cursor para o início do enumerador.</span><span class="sxs-lookup"><span data-stu-id="18001-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="18001-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="18001-105">Quick info</span></span>

<span data-ttu-id="18001-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="18001-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="18001-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="18001-107">Parameters</span></span>

<span data-ttu-id="18001-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="18001-108">_ppclone_</span></span>
  
> <span data-ttu-id="18001-109">[out] Um ponteiro para o ponteiro para a cópia da interface [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="18001-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="18001-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="18001-110">Return values</span></span>

|<span data-ttu-id="18001-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="18001-111">**HRESULT**</span></span>|<span data-ttu-id="18001-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18001-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18001-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="18001-113">S_OK</span></span>  <br/> |<span data-ttu-id="18001-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="18001-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="18001-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="18001-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="18001-116">Não há memória suficiente para tornar a cópia.</span><span class="sxs-lookup"><span data-stu-id="18001-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18001-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="18001-117">See also</span></span>

- [<span data-ttu-id="18001-118">Constantes (API de livre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="18001-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="18001-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="18001-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="18001-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="18001-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="18001-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="18001-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="18001-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="18001-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)


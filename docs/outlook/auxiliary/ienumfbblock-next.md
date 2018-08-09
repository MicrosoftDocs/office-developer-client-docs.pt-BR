---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765826"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="afdc5-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="afdc5-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="afdc5-104">Obtém o próximo número especificado de blocos de informações de disponibilidade de dados em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="afdc5-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="afdc5-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="afdc5-105">Quick info</span></span>

<span data-ttu-id="afdc5-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="afdc5-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="afdc5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afdc5-107">Parameters</span></span>

<span data-ttu-id="afdc5-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="afdc5-108">_celt_</span></span>
  
> <span data-ttu-id="afdc5-109">[in] O número de livre/ocupado dados blocos no *pblk* para recuperar.</span><span class="sxs-lookup"><span data-stu-id="afdc5-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="afdc5-110">_PBLK_</span><span class="sxs-lookup"><span data-stu-id="afdc5-110">_pblk_</span></span>
  
> <span data-ttu-id="afdc5-111">[in] Um ponteiro para uma matriz de blocos de livre/ocupado.</span><span class="sxs-lookup"><span data-stu-id="afdc5-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="afdc5-112">A matriz é alocada um tamanho de *celt* .</span><span class="sxs-lookup"><span data-stu-id="afdc5-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="afdc5-113">Os blocos de livre/ocupado solicitados são retornados nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="afdc5-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="afdc5-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="afdc5-114">_pcfetch_</span></span>
  
> <span data-ttu-id="afdc5-115">[out] O número de blocos de livre/ocupado realmente retornados em *pblk* .</span><span class="sxs-lookup"><span data-stu-id="afdc5-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="afdc5-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="afdc5-116">Return values</span></span>

|<span data-ttu-id="afdc5-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="afdc5-117">**HRESULT**</span></span>|<span data-ttu-id="afdc5-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="afdc5-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="afdc5-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="afdc5-119">S_OK</span></span>  <br/> |<span data-ttu-id="afdc5-120">O número de blocos solicitado foi retornado.</span><span class="sxs-lookup"><span data-stu-id="afdc5-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="afdc5-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="afdc5-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="afdc5-122">O número de blocos solicitado não foi retornado.</span><span class="sxs-lookup"><span data-stu-id="afdc5-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afdc5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="afdc5-123">See also</span></span>

- [<span data-ttu-id="afdc5-124">Constantes (API de livre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="afdc5-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="afdc5-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="afdc5-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="afdc5-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="afdc5-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="afdc5-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="afdc5-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="afdc5-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="afdc5-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="afdc5-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="afdc5-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)


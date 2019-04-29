---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422135"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="50ece-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="50ece-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="50ece-104">Obtém o próximo número específico de blocos de disponibilidade de dados em uma enumeração.</span><span class="sxs-lookup"><span data-stu-id="50ece-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="50ece-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="50ece-105">Quick info</span></span>

<span data-ttu-id="50ece-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="50ece-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="50ece-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50ece-107">Parameters</span></span>

<span data-ttu-id="50ece-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="50ece-108">_celt_</span></span>
  
> <span data-ttu-id="50ece-109">no O número de blocos de dados de disponibilidade no *pblk* a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="50ece-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="50ece-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="50ece-110">_pblk_</span></span>
  
> <span data-ttu-id="50ece-111">no Um ponteiro para uma matriz de blocos de disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="50ece-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="50ece-112">A matriz é alocada com um tamanho de *celt* .</span><span class="sxs-lookup"><span data-stu-id="50ece-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="50ece-113">Os blocos de disponibilidade solicitados são retornados nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="50ece-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="50ece-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="50ece-114">_pcfetch_</span></span>
  
> <span data-ttu-id="50ece-115">bota O número de blocos de disponibilidade realmente retornados no *pblk* .</span><span class="sxs-lookup"><span data-stu-id="50ece-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="50ece-116">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="50ece-116">Return values</span></span>

|<span data-ttu-id="50ece-117">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="50ece-117">**HRESULT**</span></span>|<span data-ttu-id="50ece-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50ece-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50ece-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="50ece-119">S_OK</span></span>  <br/> |<span data-ttu-id="50ece-120">O número solicitado de blocos foi retornado.</span><span class="sxs-lookup"><span data-stu-id="50ece-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="50ece-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="50ece-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="50ece-122">O número solicitado de blocos não foi retornado.</span><span class="sxs-lookup"><span data-stu-id="50ece-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50ece-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="50ece-123">See also</span></span>

- [<span data-ttu-id="50ece-124">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="50ece-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="50ece-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="50ece-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="50ece-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="50ece-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="50ece-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="50ece-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="50ece-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="50ece-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="50ece-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="50ece-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)


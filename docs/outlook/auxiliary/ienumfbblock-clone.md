---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413399"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="bc6e4-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="bc6e4-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="bc6e4-104">Cria uma cópia do enumerador, usando a mesma restrição de tempo, mas definindo o cursor para o início do enumerador.</span><span class="sxs-lookup"><span data-stu-id="bc6e4-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bc6e4-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="bc6e4-105">Quick info</span></span>

<span data-ttu-id="bc6e4-106">Consulte [IEnumFBBlock](ienumfbblock.md).</span><span class="sxs-lookup"><span data-stu-id="bc6e4-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="bc6e4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc6e4-107">Parameters</span></span>

<span data-ttu-id="bc6e4-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="bc6e4-108">_ppclone_</span></span>
  
> <span data-ttu-id="bc6e4-109">bota Um ponteiro para ponteiro para a cópia da interface [IEnumFBBlock](ienumfbblock.md) .</span><span class="sxs-lookup"><span data-stu-id="bc6e4-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bc6e4-110">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="bc6e4-110">Return values</span></span>

|<span data-ttu-id="bc6e4-111">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bc6e4-111">**HRESULT**</span></span>|<span data-ttu-id="bc6e4-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bc6e4-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc6e4-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bc6e4-113">S_OK</span></span>  <br/> |<span data-ttu-id="bc6e4-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bc6e4-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="bc6e4-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="bc6e4-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="bc6e4-116">Não há memória suficiente para fazer a cópia.</span><span class="sxs-lookup"><span data-stu-id="bc6e4-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc6e4-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc6e4-117">See also</span></span>

- [<span data-ttu-id="bc6e4-118">Constantes (API do serviço de disponibilidade)</span><span class="sxs-lookup"><span data-stu-id="bc6e4-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="bc6e4-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="bc6e4-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="bc6e4-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="bc6e4-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="bc6e4-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="bc6e4-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="bc6e4-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="bc6e4-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)


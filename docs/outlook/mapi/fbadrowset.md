---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341017"
---
# <a name="fbadrowset"></a><span data-ttu-id="500d2-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="500d2-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="500d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="500d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="500d2-105">Valida todas as linhas de tabela incluídas em um conjunto de linhas de tabela.</span><span class="sxs-lookup"><span data-stu-id="500d2-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="500d2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="500d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="500d2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="500d2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="500d2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="500d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="500d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="500d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="500d2-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="500d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="500d2-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="500d2-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="500d2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="500d2-112">Parameters</span></span>

 <span data-ttu-id="500d2-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="500d2-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="500d2-114">no Ponteiro para uma estrutura [SRowSet](srowset.md) identificando o conjunto de linhas a ser validado.</span><span class="sxs-lookup"><span data-stu-id="500d2-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="500d2-115">Se o ponteiro for NULL, a estrutura é inválida.</span><span class="sxs-lookup"><span data-stu-id="500d2-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="500d2-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="500d2-116">Return value</span></span>

<span data-ttu-id="500d2-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="500d2-117">TRUE</span></span> 
  
> <span data-ttu-id="500d2-118">Uma linha do conjunto de linhas especificado é inválida ou o próprio conjunto de linhas é inválido.</span><span class="sxs-lookup"><span data-stu-id="500d2-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="500d2-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="500d2-119">FALSE</span></span> 
  
> <span data-ttu-id="500d2-120">As linhas do conjunto de linhas especificado e o próprio conjunto de linhas são válidas.</span><span class="sxs-lookup"><span data-stu-id="500d2-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="500d2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="500d2-121">See also</span></span>



[<span data-ttu-id="500d2-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="500d2-122">FBadRow</span></span>](fbadrow.md)


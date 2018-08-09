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
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766559"
---
# <a name="fbadrowset"></a><span data-ttu-id="11bd1-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="11bd1-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="11bd1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11bd1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11bd1-105">Valida todas as linhas de tabela incluídas em um conjunto de linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="11bd1-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11bd1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="11bd1-106">Header file:</span></span>  <br/> |<span data-ttu-id="11bd1-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="11bd1-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="11bd1-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="11bd1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11bd1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11bd1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11bd1-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="11bd1-110">Called by:</span></span>  <br/> |<span data-ttu-id="11bd1-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="11bd1-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="11bd1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11bd1-112">Parameters</span></span>

 <span data-ttu-id="11bd1-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="11bd1-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="11bd1-114">[in] Ponteiro para uma estrutura [SRowSet](srowset.md) que identifica a linha definida para ser validado.</span><span class="sxs-lookup"><span data-stu-id="11bd1-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="11bd1-115">Se o ponteiro for NULL, a estrutura é inválida.</span><span class="sxs-lookup"><span data-stu-id="11bd1-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="11bd1-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="11bd1-116">Return value</span></span>

<span data-ttu-id="11bd1-117">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="11bd1-117">TRUE</span></span> 
  
> <span data-ttu-id="11bd1-118">Uma linha do conjunto de linha especificada é inválida ou linha do próprio conjunto é inválida.</span><span class="sxs-lookup"><span data-stu-id="11bd1-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="11bd1-119">FALSO</span><span class="sxs-lookup"><span data-stu-id="11bd1-119">FALSE</span></span> 
  
> <span data-ttu-id="11bd1-120">As linhas do conjunto de linha especificada e a linha definida em si são válidos.</span><span class="sxs-lookup"><span data-stu-id="11bd1-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="11bd1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="11bd1-121">See also</span></span>



[<span data-ttu-id="11bd1-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="11bd1-122">FBadRow</span></span>](fbadrow.md)


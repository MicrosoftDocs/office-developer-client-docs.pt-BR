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
ms.openlocfilehash: e86e9fbf4901b5944775886f38db1ba12c4b122d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590957"
---
# <a name="fbadrowset"></a><span data-ttu-id="bbe98-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="bbe98-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="bbe98-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbe98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbe98-105">Valida todas as linhas de tabela incluídas em um conjunto de linhas da tabela.</span><span class="sxs-lookup"><span data-stu-id="bbe98-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bbe98-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bbe98-106">Header file:</span></span>  <br/> |<span data-ttu-id="bbe98-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="bbe98-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="bbe98-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="bbe98-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bbe98-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bbe98-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bbe98-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="bbe98-110">Called by:</span></span>  <br/> |<span data-ttu-id="bbe98-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="bbe98-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="bbe98-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbe98-112">Parameters</span></span>

 <span data-ttu-id="bbe98-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="bbe98-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="bbe98-114">[in] Ponteiro para uma estrutura [SRowSet](srowset.md) que identifica a linha definida para ser validado.</span><span class="sxs-lookup"><span data-stu-id="bbe98-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="bbe98-115">Se o ponteiro for NULL, a estrutura é inválida.</span><span class="sxs-lookup"><span data-stu-id="bbe98-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbe98-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bbe98-116">Return value</span></span>

<span data-ttu-id="bbe98-117">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="bbe98-117">TRUE</span></span> 
  
> <span data-ttu-id="bbe98-118">Uma linha do conjunto de linha especificada é inválida ou linha do próprio conjunto é inválida.</span><span class="sxs-lookup"><span data-stu-id="bbe98-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="bbe98-119">FALSO</span><span class="sxs-lookup"><span data-stu-id="bbe98-119">FALSE</span></span> 
  
> <span data-ttu-id="bbe98-120">As linhas do conjunto de linha especificada e a linha definida em si são válidos.</span><span class="sxs-lookup"><span data-stu-id="bbe98-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbe98-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbe98-121">See also</span></span>



[<span data-ttu-id="bbe98-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="bbe98-122">FBadRow</span></span>](fbadrow.md)


---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 23b4ed78f4b65a5af4c2f3e11fa770030fe4eeee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590159"
---
# <a name="fbadrow"></a><span data-ttu-id="d48cd-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="d48cd-103">FBadRow</span></span>

  
  
<span data-ttu-id="d48cd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d48cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d48cd-105">Valida uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="d48cd-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d48cd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d48cd-106">Header file:</span></span>  <br/> |<span data-ttu-id="d48cd-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d48cd-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d48cd-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="d48cd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d48cd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d48cd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d48cd-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="d48cd-110">Called by:</span></span>  <br/> |<span data-ttu-id="d48cd-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="d48cd-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="d48cd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d48cd-112">Parameters</span></span>

 <span data-ttu-id="d48cd-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="d48cd-113">_lprow_</span></span>
  
> <span data-ttu-id="d48cd-114">[in] Ponteiro para uma estrutura [SRow](srow.md) que identifica a linha a ser validado.</span><span class="sxs-lookup"><span data-stu-id="d48cd-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d48cd-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d48cd-115">Return value</span></span>

<span data-ttu-id="d48cd-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="d48cd-116">TRUE</span></span> 
  
> <span data-ttu-id="d48cd-117">A linha especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="d48cd-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="d48cd-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="d48cd-118">FALSE</span></span> 
  
> <span data-ttu-id="d48cd-119">A linha especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="d48cd-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d48cd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d48cd-120">See also</span></span>



[<span data-ttu-id="d48cd-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="d48cd-121">FBadRowSet</span></span>](fbadrowset.md)


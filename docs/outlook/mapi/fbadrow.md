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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c3025c353c71958a19303c5e79cec319a3bf8015
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766552"
---
# <a name="fbadrow"></a><span data-ttu-id="352b8-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="352b8-103">FBadRow</span></span>

  
  
<span data-ttu-id="352b8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="352b8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="352b8-105">Valida uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="352b8-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="352b8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="352b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="352b8-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="352b8-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="352b8-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="352b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="352b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="352b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="352b8-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="352b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="352b8-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="352b8-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="352b8-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="352b8-112">Parameters</span></span>

 <span data-ttu-id="352b8-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="352b8-113">_lprow_</span></span>
  
> <span data-ttu-id="352b8-114">[in] Ponteiro para uma estrutura [SRow](srow.md) que identifica a linha a ser validado.</span><span class="sxs-lookup"><span data-stu-id="352b8-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="352b8-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="352b8-115">Return value</span></span>

<span data-ttu-id="352b8-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="352b8-116">TRUE</span></span> 
  
> <span data-ttu-id="352b8-117">A linha especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="352b8-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="352b8-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="352b8-118">FALSE</span></span> 
  
> <span data-ttu-id="352b8-119">A linha especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="352b8-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="352b8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="352b8-120">See also</span></span>



[<span data-ttu-id="352b8-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="352b8-121">FBadRowSet</span></span>](fbadrowset.md)


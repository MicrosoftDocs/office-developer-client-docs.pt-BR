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
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420616"
---
# <a name="fbadrow"></a><span data-ttu-id="84318-103">FBadRow</span><span class="sxs-lookup"><span data-stu-id="84318-103">FBadRow</span></span>

  
  
<span data-ttu-id="84318-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84318-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84318-105">Valida uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="84318-105">Validates a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84318-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="84318-106">Header file:</span></span>  <br/> |<span data-ttu-id="84318-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="84318-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="84318-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="84318-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="84318-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="84318-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="84318-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="84318-110">Called by:</span></span>  <br/> |<span data-ttu-id="84318-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="84318-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a><span data-ttu-id="84318-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84318-112">Parameters</span></span>

 <span data-ttu-id="84318-113">_lprow_</span><span class="sxs-lookup"><span data-stu-id="84318-113">_lprow_</span></span>
  
> <span data-ttu-id="84318-114">no Ponteiro para uma estrutura [SRow](srow.md) identificando a linha a ser validada.</span><span class="sxs-lookup"><span data-stu-id="84318-114">[in] Pointer to an [SRow](srow.md) structure identifying the row to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="84318-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="84318-115">Return value</span></span>

<span data-ttu-id="84318-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="84318-116">TRUE</span></span> 
  
> <span data-ttu-id="84318-117">A linha especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="84318-117">The specified row is invalid.</span></span>
    
<span data-ttu-id="84318-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="84318-118">FALSE</span></span> 
  
> <span data-ttu-id="84318-119">A linha especificada é válida.</span><span class="sxs-lookup"><span data-stu-id="84318-119">The specified row is valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84318-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="84318-120">See also</span></span>



[<span data-ttu-id="84318-121">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="84318-121">FBadRowSet</span></span>](fbadrowset.md)


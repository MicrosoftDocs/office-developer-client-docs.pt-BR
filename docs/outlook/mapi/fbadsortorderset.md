---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766533"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="b65d7-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b65d7-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="b65d7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b65d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b65d7-105">Valida uma ordem de classificação definida verificando sua alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="b65d7-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b65d7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b65d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="b65d7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b65d7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b65d7-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b65d7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b65d7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b65d7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b65d7-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b65d7-110">Called by:</span></span>  <br/> |<span data-ttu-id="b65d7-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b65d7-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="b65d7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b65d7-112">Parameters</span></span>

 <span data-ttu-id="b65d7-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="b65d7-113">_lpsos_</span></span>
  
> <span data-ttu-id="b65d7-114">[in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação, defina a ser validado.</span><span class="sxs-lookup"><span data-stu-id="b65d7-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b65d7-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b65d7-115">Return value</span></span>

<span data-ttu-id="b65d7-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b65d7-116">TRUE</span></span> 
  
> <span data-ttu-id="b65d7-117">O conjunto de ordem de classificação especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="b65d7-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="b65d7-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="b65d7-118">FALSE</span></span> 
  
> <span data-ttu-id="b65d7-119">O conjunto de ordem de classificação especificada é válido.</span><span class="sxs-lookup"><span data-stu-id="b65d7-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b65d7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b65d7-120">Remarks</span></span>

<span data-ttu-id="b65d7-121">A função de **FBadSortOrderSet** pode ser usada para se preparar para uma chamada para um método de classificação, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="b65d7-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  


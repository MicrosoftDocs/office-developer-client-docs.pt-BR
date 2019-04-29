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
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428456"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="4ebff-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="4ebff-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="4ebff-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ebff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ebff-105">Valida uma ordem de classificação definida verificando sua alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="4ebff-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ebff-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4ebff-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ebff-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="4ebff-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="4ebff-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4ebff-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ebff-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ebff-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4ebff-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="4ebff-110">Called by:</span></span>  <br/> |<span data-ttu-id="4ebff-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="4ebff-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="4ebff-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ebff-112">Parameters</span></span>

 <span data-ttu-id="4ebff-113">_Lpsos_</span><span class="sxs-lookup"><span data-stu-id="4ebff-113">_lpsos_</span></span>
  
> <span data-ttu-id="4ebff-114">no Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) identificando a ordem de classificação definida para ser validada.</span><span class="sxs-lookup"><span data-stu-id="4ebff-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4ebff-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4ebff-115">Return value</span></span>

<span data-ttu-id="4ebff-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="4ebff-116">TRUE</span></span> 
  
> <span data-ttu-id="4ebff-117">O conjunto de ordem de classificação especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="4ebff-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="4ebff-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ebff-118">FALSE</span></span> 
  
> <span data-ttu-id="4ebff-119">O conjunto de ordem de classificação especificado é válido.</span><span class="sxs-lookup"><span data-stu-id="4ebff-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ebff-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ebff-120">Remarks</span></span>

<span data-ttu-id="4ebff-121">A função **FBadSortOrderSet** pode ser usada para preparar uma chamada para um método Sort, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebff-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  


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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578574"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="3a084-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="3a084-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="3a084-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a084-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a084-105">Valida uma ordem de classificação definida verificando sua alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="3a084-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a084-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3a084-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a084-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="3a084-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="3a084-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3a084-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a084-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3a084-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3a084-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3a084-110">Called by:</span></span>  <br/> |<span data-ttu-id="3a084-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="3a084-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="3a084-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a084-112">Parameters</span></span>

 <span data-ttu-id="3a084-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="3a084-113">_lpsos_</span></span>
  
> <span data-ttu-id="3a084-114">[in] Ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que identifica a ordem de classificação, defina a ser validado.</span><span class="sxs-lookup"><span data-stu-id="3a084-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3a084-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3a084-115">Return value</span></span>

<span data-ttu-id="3a084-116">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="3a084-116">TRUE</span></span> 
  
> <span data-ttu-id="3a084-117">O conjunto de ordem de classificação especificado é inválido.</span><span class="sxs-lookup"><span data-stu-id="3a084-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="3a084-118">FALSO</span><span class="sxs-lookup"><span data-stu-id="3a084-118">FALSE</span></span> 
  
> <span data-ttu-id="3a084-119">O conjunto de ordem de classificação especificada é válido.</span><span class="sxs-lookup"><span data-stu-id="3a084-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a084-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a084-120">Remarks</span></span>

<span data-ttu-id="3a084-121">A função de **FBadSortOrderSet** pode ser usada para se preparar para uma chamada para um método de classificação, como o método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="3a084-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  


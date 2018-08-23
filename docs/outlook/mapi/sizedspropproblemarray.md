---
title: SizedSPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropProblemArray
api_type:
- COM
ms.assetid: 2fc3febb-8c69-4315-a112-a28eee98013d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bbced8412c2c3438c58af74ef072a46606b59ddc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594611"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="ba4a8-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ba4a8-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="ba4a8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba4a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba4a8-105">Cria uma estrutura [SPropProblemArray](spropproblemarray.md) nomeada que contém um número especificado de estruturas de [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="ba4a8-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba4a8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ba4a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba4a8-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba4a8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ba4a8-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="ba4a8-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ba4a8-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="ba4a8-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="ba4a8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba4a8-110">Parameters</span></span>

<span data-ttu-id="ba4a8-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="ba4a8-111">__cprob_</span></span>
  
> <span data-ttu-id="ba4a8-112">Contagem de estruturas de **SPropProblem** a serem incluídos na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ba4a8-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="ba4a8-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="ba4a8-113">__name_</span></span>
  
> <span data-ttu-id="ba4a8-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ba4a8-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba4a8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba4a8-115">Remarks</span></span>

<span data-ttu-id="ba4a8-116">Use a macro **SizedSPropProblemArray** para criar uma matriz de problema de propriedade com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="ba4a8-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="ba4a8-117">Para usar a nova estrutura que é resultado da macro **SizedSPropProblemArray** como um ponteiro para uma estrutura **SPropProblemArray** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="ba4a8-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="ba4a8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba4a8-118">See also</span></span>

- [<span data-ttu-id="ba4a8-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="ba4a8-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="ba4a8-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="ba4a8-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="ba4a8-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="ba4a8-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


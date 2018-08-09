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
ms.openlocfilehash: b8521172b441bd26a6562aa28f836d453544928f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770419"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="d623d-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d623d-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="d623d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d623d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d623d-105">Cria uma estrutura [SPropProblemArray](spropproblemarray.md) nomeada que contém um número especificado de estruturas de [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="d623d-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d623d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d623d-106">Header file:</span></span>  <br/> |<span data-ttu-id="d623d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d623d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d623d-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="d623d-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d623d-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="d623d-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="d623d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d623d-110">Parameters</span></span>

<span data-ttu-id="d623d-111">__cprob_</span><span class="sxs-lookup"><span data-stu-id="d623d-111">__cprob_</span></span>
  
> <span data-ttu-id="d623d-112">Contagem de estruturas de **SPropProblem** a serem incluídos na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="d623d-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="d623d-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="d623d-113">__name_</span></span>
  
> <span data-ttu-id="d623d-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="d623d-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d623d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d623d-115">Remarks</span></span>

<span data-ttu-id="d623d-116">Use a macro **SizedSPropProblemArray** para criar uma matriz de problema de propriedade com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="d623d-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="d623d-117">Para usar a nova estrutura que é resultado da macro **SizedSPropProblemArray** como um ponteiro para uma estrutura **SPropProblemArray** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="d623d-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="d623d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d623d-118">See also</span></span>

- [<span data-ttu-id="d623d-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="d623d-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="d623d-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="d623d-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="d623d-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="d623d-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


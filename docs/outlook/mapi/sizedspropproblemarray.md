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
ms.openlocfilehash: b3818e5e1429c7e2b7d5f7533db733ba29e672c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418110"
---
# <a name="sizedspropproblemarray"></a><span data-ttu-id="7d87f-103">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7d87f-103">SizedSPropProblemArray</span></span>

<span data-ttu-id="7d87f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d87f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d87f-105">Cria uma estrutura [SPropProblemArray](spropproblemarray.md) nomeada que contém um número especificado de [estruturas SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="7d87f-105">Creates a named [SPropProblemArray](spropproblemarray.md) structure that contains a specified number of [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d87f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7d87f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d87f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d87f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7d87f-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7d87f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7d87f-109">**SPropProblemArray**</span><span class="sxs-lookup"><span data-stu-id="7d87f-109">**SPropProblemArray**</span></span> <br/> |
   
```cpp
SizedSPropProblemArray(_cprob, _name)
```

## <a name="parameters"></a><span data-ttu-id="7d87f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d87f-110">Parameters</span></span>

<span data-ttu-id="7d87f-111">_ _cprob_</span><span class="sxs-lookup"><span data-stu-id="7d87f-111">_ _cprob_</span></span>
  
> <span data-ttu-id="7d87f-112">Contagem de **estruturas SPropProblem** a serem incluídas na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="7d87f-112">Count of **SPropProblem** structures to be included in the new structure.</span></span> 
    
<span data-ttu-id="7d87f-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="7d87f-113">_ _name_</span></span>
  
> <span data-ttu-id="7d87f-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="7d87f-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d87f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d87f-115">Remarks</span></span>

<span data-ttu-id="7d87f-116">Use a macro **SizedSPropProblemArray** para criar uma matriz de problemas de propriedade com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="7d87f-116">Use the **SizedSPropProblemArray** macro to create a property problem array with explicit bounds.</span></span> <span data-ttu-id="7d87f-117">Para usar a nova estrutura que resulta da macro **SizedSPropProblemArray** como um ponteiro para uma estrutura **SPropProblemArray,** execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="7d87f-117">To use the new structure that results from the **SizedSPropProblemArray** macro as a pointer to an **SPropProblemArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropProbArray = (LPSPropProblemArray) &SizedSPropProblemArray;
```

## <a name="see-also"></a><span data-ttu-id="7d87f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d87f-118">See also</span></span>

- [<span data-ttu-id="7d87f-119">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7d87f-119">SPropProblemArray</span></span>](spropproblemarray.md)
- [<span data-ttu-id="7d87f-120">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="7d87f-120">SPropProblem</span></span>](spropproblem.md)
- [<span data-ttu-id="7d87f-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="7d87f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


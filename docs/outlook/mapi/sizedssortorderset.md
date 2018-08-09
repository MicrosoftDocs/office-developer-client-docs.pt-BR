---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2eb92c3f1555407a77332bd6ec3b2b7202f0553f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770437"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="236e4-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="236e4-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="236e4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="236e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="236e4-105">Cria uma estrutura [SSortOrderSet](ssortorderset.md) nomeada que contém um número especificado de ordens de classificação.</span><span class="sxs-lookup"><span data-stu-id="236e4-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="236e4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="236e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="236e4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="236e4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="236e4-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="236e4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="236e4-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="236e4-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="236e4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="236e4-110">Parameters</span></span>

<span data-ttu-id="236e4-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="236e4-111">__csort_</span></span>
  
> <span data-ttu-id="236e4-112">Contagem de ordens de classificação a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="236e4-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="236e4-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="236e4-113">__name_</span></span>
  
> <span data-ttu-id="236e4-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="236e4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="236e4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="236e4-115">Remarks</span></span>

<span data-ttu-id="236e4-116">Use a macro **SizedSSortOrderSet** para criar uma ordem de classificação definida com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="236e4-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="236e4-117">Para usar a nova estrutura que é resultado da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="236e4-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="236e4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="236e4-118">See also</span></span>

- [<span data-ttu-id="236e4-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="236e4-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="236e4-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="236e4-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


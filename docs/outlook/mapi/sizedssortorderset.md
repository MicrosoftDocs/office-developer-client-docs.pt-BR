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
ms.openlocfilehash: 7622baaebf6918cf84c48e53291cf5ec2c0b1a4a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572561"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="ffb6d-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ffb6d-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="ffb6d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffb6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffb6d-105">Cria uma estrutura [SSortOrderSet](ssortorderset.md) nomeada que contém um número especificado de ordens de classificação.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ffb6d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ffb6d-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffb6d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ffb6d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ffb6d-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="ffb6d-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ffb6d-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="ffb6d-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="ffb6d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffb6d-110">Parameters</span></span>

<span data-ttu-id="ffb6d-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="ffb6d-111">__csort_</span></span>
  
> <span data-ttu-id="ffb6d-112">Contagem de ordens de classificação a ser incluído na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="ffb6d-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="ffb6d-113">__name_</span></span>
  
> <span data-ttu-id="ffb6d-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ffb6d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffb6d-115">Remarks</span></span>

<span data-ttu-id="ffb6d-116">Use a macro **SizedSSortOrderSet** para criar uma ordem de classificação definida com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="ffb6d-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="ffb6d-117">Para usar a nova estrutura que é resultado da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="ffb6d-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="ffb6d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffb6d-118">See also</span></span>

- [<span data-ttu-id="ffb6d-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ffb6d-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="ffb6d-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="ffb6d-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


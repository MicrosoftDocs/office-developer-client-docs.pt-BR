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
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282625"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="1d200-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1d200-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="1d200-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d200-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d200-105">Cria uma estrutura nomeada do [SSortOrderSet](ssortorderset.md) que contém um número especificado de pedidos de classificação.</span><span class="sxs-lookup"><span data-stu-id="1d200-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d200-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1d200-106">Header file:</span></span>  <br/> |<span data-ttu-id="1d200-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1d200-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1d200-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="1d200-108">Related structure:</span></span>  <br/> |<span data-ttu-id="1d200-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="1d200-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="1d200-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d200-110">Parameters</span></span>

<span data-ttu-id="1d200-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="1d200-111">__csort_</span></span>
  
> <span data-ttu-id="1d200-112">Contagem de ordens de classificação a serem incluídas na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="1d200-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="1d200-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="1d200-113">__name_</span></span>
  
> <span data-ttu-id="1d200-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="1d200-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d200-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d200-115">Remarks</span></span>

<span data-ttu-id="1d200-116">Use a macro **SizedSSortOrderSet** para criar um conjunto de ordem de classificação com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="1d200-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="1d200-117">Para usar a nova estrutura que resulta da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="1d200-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="1d200-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d200-118">See also</span></span>

- [<span data-ttu-id="1d200-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="1d200-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="1d200-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="1d200-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


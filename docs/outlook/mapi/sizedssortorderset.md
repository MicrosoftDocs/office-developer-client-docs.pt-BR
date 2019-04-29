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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428603"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="800a5-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="800a5-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="800a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="800a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="800a5-105">Cria uma estrutura nomeada do [SSortOrderSet](ssortorderset.md) que contém um número especificado de pedidos de classificação.</span><span class="sxs-lookup"><span data-stu-id="800a5-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="800a5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="800a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="800a5-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="800a5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="800a5-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="800a5-108">Related structure:</span></span>  <br/> |<span data-ttu-id="800a5-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="800a5-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="800a5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="800a5-110">Parameters</span></span>

<span data-ttu-id="800a5-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="800a5-111">__csort_</span></span>
  
> <span data-ttu-id="800a5-112">Contagem de ordens de classificação a serem incluídas na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="800a5-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="800a5-113">__nome_</span><span class="sxs-lookup"><span data-stu-id="800a5-113">__name_</span></span>
  
> <span data-ttu-id="800a5-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="800a5-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="800a5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="800a5-115">Remarks</span></span>

<span data-ttu-id="800a5-116">Use a macro **SizedSSortOrderSet** para criar um conjunto de ordem de classificação com limites explícitos.</span><span class="sxs-lookup"><span data-stu-id="800a5-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="800a5-117">Para usar a nova estrutura que resulta da macro **SizedSSortOrderSet** como um ponteiro para uma estrutura **SSortOrderSet** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="800a5-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="800a5-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="800a5-118">See also</span></span>

- [<span data-ttu-id="800a5-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="800a5-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="800a5-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="800a5-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


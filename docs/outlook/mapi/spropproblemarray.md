---
title: SPropProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblemArray
api_type:
- COM
ms.assetid: 3fbaa77a-be43-4fce-af67-1826ee101799
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e71658922b6cb80dadc7e034a51c10189c4207ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568494"
---
# <a name="spropproblemarray"></a><span data-ttu-id="3c641-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="3c641-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="3c641-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c641-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c641-105">Contém uma matriz de uma ou mais estruturas de [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="3c641-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c641-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3c641-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c641-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c641-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3c641-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="3c641-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="3c641-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="3c641-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="3c641-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="3c641-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="3c641-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="3c641-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="3c641-112">Members</span><span class="sxs-lookup"><span data-stu-id="3c641-112">Members</span></span>

 <span data-ttu-id="3c641-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="3c641-113">**cProblem**</span></span>
  
> <span data-ttu-id="3c641-114">Contagem de estruturas de [SPropProblem](spropproblem.md) na matriz indicado pelo membro **aProblem** .</span><span class="sxs-lookup"><span data-stu-id="3c641-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="3c641-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="3c641-115">**aProblem**</span></span>
  
> <span data-ttu-id="3c641-116">Matriz de estruturas de **SPropProblem** , cada uma descrevendo um erro de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3c641-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3c641-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c641-117">Remarks</span></span>

<span data-ttu-id="3c641-118">Para obter mais informações sobre como as estruturas **SPropProblem** e **SPropProblemArray** funcionam com erros relacionados às propriedades, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3c641-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c641-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c641-119">See also</span></span>



[<span data-ttu-id="3c641-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="3c641-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="3c641-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="3c641-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="3c641-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="3c641-122">MAPI Structures</span></span>](mapi-structures.md)


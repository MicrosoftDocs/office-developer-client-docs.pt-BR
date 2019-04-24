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
ms.openlocfilehash: f78e0ed939e190a9855ea4b040d18c01cfecc91d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357838"
---
# <a name="spropproblemarray"></a><span data-ttu-id="c1ca8-103">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c1ca8-103">SPropProblemArray</span></span>

  
  
<span data-ttu-id="c1ca8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1ca8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1ca8-105">Contém uma matriz de uma ou mais estruturas [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ca8-105">Contains an array of one or more [SPropProblem](spropproblem.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c1ca8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c1ca8-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1ca8-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c1ca8-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c1ca8-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="c1ca8-108">Related macros:</span></span>  <br/> |[<span data-ttu-id="c1ca8-109">CbNewSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c1ca8-109">CbNewSPropProblemArray</span></span>](cbnewspropproblemarray.md) <br/> [<span data-ttu-id="c1ca8-110">CbSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c1ca8-110">CbSPropProblemArray</span></span>](cbspropproblemarray.md) <br/> [<span data-ttu-id="c1ca8-111">SizedSPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="c1ca8-111">SizedSPropProblemArray</span></span>](sizedspropproblemarray.md) <br/> |
   
```cpp
typedef struct _SPropProblemArray
{
  ULONG cProblem;
  SPropProblem aProblem[MAPI_DIM];
} SPropProblemArray, FAR *LPSPropProblemArray;

```

## <a name="members"></a><span data-ttu-id="c1ca8-112">Members</span><span class="sxs-lookup"><span data-stu-id="c1ca8-112">Members</span></span>

 <span data-ttu-id="c1ca8-113">**cProblem**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-113">**cProblem**</span></span>
  
> <span data-ttu-id="c1ca8-114">Contagem de estruturas [SPropProblem](spropproblem.md) na matriz indicada pelo membro **aproblem** .</span><span class="sxs-lookup"><span data-stu-id="c1ca8-114">Count of [SPropProblem](spropproblem.md) structures in the array indicated by the **aProblem** member.</span></span> 
    
 <span data-ttu-id="c1ca8-115">**aProblem**</span><span class="sxs-lookup"><span data-stu-id="c1ca8-115">**aProblem**</span></span>
  
> <span data-ttu-id="c1ca8-116">Matriz de estruturas **SPropProblem** , cada uma descrevendo um erro de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c1ca8-116">Array of **SPropProblem** structures, each describing a property error.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1ca8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1ca8-117">Remarks</span></span>

<span data-ttu-id="c1ca8-118">Para obter mais informações sobre como as estruturas **SPropProblem** e **SPropProblemArray** funcionam com erros relacionados a propriedades, consulte [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c1ca8-118">For more information about how the **SPropProblem** and **SPropProblemArray** structures work with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1ca8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1ca8-119">See also</span></span>



[<span data-ttu-id="c1ca8-120">SCODE</span><span class="sxs-lookup"><span data-stu-id="c1ca8-120">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="c1ca8-121">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="c1ca8-121">SPropProblem</span></span>](spropproblem.md)


[<span data-ttu-id="c1ca8-122">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c1ca8-122">MAPI Structures</span></span>](mapi-structures.md)


---
title: SMAPIVerbArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerbArray
api_type:
- COM
ms.assetid: 8736f75c-3e95-42dd-9bc1-2f0bd23c4a02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7cba5dce60ce15ddb12776d619143849298aac9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357474"
---
# <a name="smapiverbarray"></a><span data-ttu-id="9c3d0-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="9c3d0-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="9c3d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c3d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c3d0-105">Contém uma matriz de estruturas [SMAPIVerb](smapiverb.md) que descrevem os verbos MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c3d0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9c3d0-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c3d0-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="9c3d0-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9c3d0-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="9c3d0-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="9c3d0-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="9c3d0-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="9c3d0-110">Members</span><span class="sxs-lookup"><span data-stu-id="9c3d0-110">Members</span></span>

 <span data-ttu-id="9c3d0-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="9c3d0-111">**cForms**</span></span>
  
> <span data-ttu-id="9c3d0-112">Contagem de verbos na matriz.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="9c3d0-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="9c3d0-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="9c3d0-114">Matriz de verbos MAPI.</span><span class="sxs-lookup"><span data-stu-id="9c3d0-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c3d0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c3d0-115">Remarks</span></span>

<span data-ttu-id="9c3d0-116">A estrutura **SMAPIVerbArray** é passada como um parâmetro no método [IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="9c3d0-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c3d0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c3d0-117">See also</span></span>



[<span data-ttu-id="9c3d0-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="9c3d0-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="9c3d0-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="9c3d0-119">MAPI Structures</span></span>](mapi-structures.md)


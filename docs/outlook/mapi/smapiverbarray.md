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
ms.openlocfilehash: 1767c86cb5390572b95530060f2295034ed35f43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770464"
---
# <a name="smapiverbarray"></a><span data-ttu-id="b2f27-103">SMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b2f27-103">SMAPIVerbArray</span></span>

  
  
<span data-ttu-id="b2f27-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2f27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2f27-105">Contém uma matriz de estruturas de [SMAPIVerb](smapiverb.md) que descrevem os verbos MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2f27-105">Contains an array of [SMAPIVerb](smapiverb.md) structures that describe MAPI verbs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2f27-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b2f27-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2f27-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="b2f27-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b2f27-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="b2f27-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b2f27-109">CbMAPIVerbArray</span><span class="sxs-lookup"><span data-stu-id="b2f27-109">CbMAPIVerbArray</span></span>](cbmapiverbarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMAPIVerb;
  SMAPIVerb aMAPIVerb[MAPI_DIM];
} SMAPIVerbArray, FAR * LPMAPIVERBARRAY;

```

## <a name="members"></a><span data-ttu-id="b2f27-110">Members</span><span class="sxs-lookup"><span data-stu-id="b2f27-110">Members</span></span>

 <span data-ttu-id="b2f27-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="b2f27-111">**cForms**</span></span>
  
> <span data-ttu-id="b2f27-112">Contagem de verbos na matriz.</span><span class="sxs-lookup"><span data-stu-id="b2f27-112">Count of verbs in the array.</span></span>
    
 <span data-ttu-id="b2f27-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="b2f27-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="b2f27-114">Matriz de verbos MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2f27-114">Array of MAPI verbs.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2f27-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2f27-115">Remarks</span></span>

<span data-ttu-id="b2f27-116">A estrutura **SMAPIVerbArray** é passada como um parâmetro no método [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f27-116">The **SMAPIVerbArray** structure is passed as a parameter in the [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2f27-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2f27-117">See also</span></span>



[<span data-ttu-id="b2f27-118">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="b2f27-118">SMAPIVerb</span></span>](smapiverb.md)


[<span data-ttu-id="b2f27-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b2f27-119">MAPI Structures</span></span>](mapi-structures.md)

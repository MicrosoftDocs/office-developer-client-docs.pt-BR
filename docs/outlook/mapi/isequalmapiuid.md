---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767695"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="9bd7f-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="9bd7f-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="9bd7f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9bd7f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9bd7f-105">Testa duas estruturas [MAPIUID](mapiuid.md) para determinar se eles contêm o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="9bd7f-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9bd7f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9bd7f-106">Header file:</span></span>  <br/> |<span data-ttu-id="9bd7f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9bd7f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9bd7f-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="9bd7f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="9bd7f-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="9bd7f-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="9bd7f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bd7f-110">Parameters</span></span>

 <span data-ttu-id="9bd7f-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="9bd7f-111">_lpuid1_</span></span>
  
> <span data-ttu-id="9bd7f-112">Ponteiro para a estrutura **MAPIUID** primeiro a ser testado.</span><span class="sxs-lookup"><span data-stu-id="9bd7f-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="9bd7f-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="9bd7f-113">_lpuid2_</span></span>
  
> <span data-ttu-id="9bd7f-114">Ponteiro para a estrutura **MAPIUID** segundo a ser testado.</span><span class="sxs-lookup"><span data-stu-id="9bd7f-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9bd7f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bd7f-115">Remarks</span></span>

<span data-ttu-id="9bd7f-116">A macro **IsEqualMAPIUID** retorna TRUE se as duas estruturas **MAPIUID** contêm o mesmo identificador e FALSE se não tiverem.</span><span class="sxs-lookup"><span data-stu-id="9bd7f-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="9bd7f-117">A macro **IsEqualMAPIUID** requer que o arquivo de cabeçalho Memory.h ser incluídos.</span><span class="sxs-lookup"><span data-stu-id="9bd7f-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bd7f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bd7f-118">See also</span></span>



[<span data-ttu-id="9bd7f-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9bd7f-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="9bd7f-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="9bd7f-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


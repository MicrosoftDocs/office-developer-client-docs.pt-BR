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
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426930"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="7a751-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="7a751-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="7a751-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a751-105">Testa duas [estruturas MAPIUID](mapiuid.md) para determinar se elas contêm o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="7a751-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a751-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7a751-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a751-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a751-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7a751-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="7a751-108">Related structure:</span></span>  <br/> |<span data-ttu-id="7a751-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="7a751-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="7a751-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a751-110">Parameters</span></span>

 <span data-ttu-id="7a751-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="7a751-111">_lpuid1_</span></span>
  
> <span data-ttu-id="7a751-112">Ponteiro para a primeira **estrutura MAPIUID** a ser testada.</span><span class="sxs-lookup"><span data-stu-id="7a751-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="7a751-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="7a751-113">_lpuid2_</span></span>
  
> <span data-ttu-id="7a751-114">Ponteiro para a segunda **estrutura MAPIUID** a ser testada.</span><span class="sxs-lookup"><span data-stu-id="7a751-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a751-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a751-115">Remarks</span></span>

<span data-ttu-id="7a751-116">A macro **IsEqualMAPIUID** retornará TRUE se as duas estruturas **MAPIUID** contêm o mesmo identificador e FALSE se não contêm.</span><span class="sxs-lookup"><span data-stu-id="7a751-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="7a751-117">A macro **IsEqualMAPIUID** requer que o arquivo de título Memory.h seja incluído.</span><span class="sxs-lookup"><span data-stu-id="7a751-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a751-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a751-118">See also</span></span>



[<span data-ttu-id="7a751-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7a751-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="7a751-120">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="7a751-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)


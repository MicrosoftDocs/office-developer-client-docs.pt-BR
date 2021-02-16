---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429870"
---
# <a name="srealarray"></a><span data-ttu-id="67e7a-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="67e7a-103">SRealArray</span></span>

  
  
<span data-ttu-id="67e7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67e7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67e7a-105">Contém uma matriz de valores flutuantes que são usados para descrever uma propriedade do tipo PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="67e7a-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67e7a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="67e7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="67e7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="67e7a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="67e7a-108">Members</span><span class="sxs-lookup"><span data-stu-id="67e7a-108">Members</span></span>

 <span data-ttu-id="67e7a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="67e7a-109">**cValues**</span></span>
  
> <span data-ttu-id="67e7a-110">Contagem de valores na matriz apontada pelo membro **lpflt.**</span><span class="sxs-lookup"><span data-stu-id="67e7a-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="67e7a-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="67e7a-111">**lpflt**</span></span>
  
> <span data-ttu-id="67e7a-112">Ponteiro para uma matriz de valores flutuantes.</span><span class="sxs-lookup"><span data-stu-id="67e7a-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67e7a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="67e7a-113">Remarks</span></span>

<span data-ttu-id="67e7a-114">Para obter mais informações sobre o PT_MV_R4 tipo de propriedade, consulte [Tipos de Propriedade.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="67e7a-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67e7a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="67e7a-115">See also</span></span>



[<span data-ttu-id="67e7a-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="67e7a-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="67e7a-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="67e7a-117">MAPI Structures</span></span>](mapi-structures.md)


---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406777"
---
# <a name="sdatetimearray"></a><span data-ttu-id="b3552-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="b3552-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="b3552-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3552-105">Contém uma matriz de valores de tempo que são usados para descrever uma propriedade do tipo PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="b3552-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3552-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b3552-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3552-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b3552-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="b3552-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3552-108">Members</span></span>

 <span data-ttu-id="b3552-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="b3552-109">**cValues**</span></span>
  
> <span data-ttu-id="b3552-110">Contagem de valores na matriz apontada pelo membro **lpft** .</span><span class="sxs-lookup"><span data-stu-id="b3552-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="b3552-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="b3552-111">**lpft**</span></span>
  
> <span data-ttu-id="b3552-112">Ponteiro para uma matriz de estruturas [FILETIME](filetime.md) que contêm os valores de hora.</span><span class="sxs-lookup"><span data-stu-id="b3552-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b3552-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3552-113">Remarks</span></span>

<span data-ttu-id="b3552-114">Para obter mais informações sobre o PT_MV_SYSTIME, confira [lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="b3552-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3552-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3552-115">See also</span></span>



[<span data-ttu-id="b3552-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="b3552-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="b3552-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="b3552-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="b3552-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="b3552-118">MAPI Structures</span></span>](mapi-structures.md)


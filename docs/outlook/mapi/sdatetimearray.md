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
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770333"
---
# <a name="sdatetimearray"></a><span data-ttu-id="5bdc7-103">SDateTimeArray</span><span class="sxs-lookup"><span data-stu-id="5bdc7-103">SDateTimeArray</span></span>

  
  
<span data-ttu-id="5bdc7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5bdc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5bdc7-105">Contém uma matriz de valores de hora são usadas para descrever uma propriedade do tipo PT_MV_SYSTIME.</span><span class="sxs-lookup"><span data-stu-id="5bdc7-105">Contains an array of time values that are used to describe a property of type PT_MV_SYSTIME.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bdc7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5bdc7-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bdc7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5bdc7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a><span data-ttu-id="5bdc7-108">Members</span><span class="sxs-lookup"><span data-stu-id="5bdc7-108">Members</span></span>

 <span data-ttu-id="5bdc7-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5bdc7-109">**cValues**</span></span>
  
> <span data-ttu-id="5bdc7-110">Contagem de valores na matriz apontado pelo membro **lpft** .</span><span class="sxs-lookup"><span data-stu-id="5bdc7-110">Count of values in the array pointed to by the **lpft** member.</span></span> 
    
 <span data-ttu-id="5bdc7-111">**lpft**</span><span class="sxs-lookup"><span data-stu-id="5bdc7-111">**lpft**</span></span>
  
> <span data-ttu-id="5bdc7-112">Ponteiro para uma matriz de estruturas [FILETIME](filetime.md) que contêm os valores de tempo.</span><span class="sxs-lookup"><span data-stu-id="5bdc7-112">Pointer to an array of [FILETIME](filetime.md) structures that contain the time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5bdc7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bdc7-113">Remarks</span></span>

<span data-ttu-id="5bdc7-114">Para obter mais informações sobre PT_MV_SYSTIME, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5bdc7-114">For more information about PT_MV_SYSTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5bdc7-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bdc7-115">See also</span></span>



[<span data-ttu-id="5bdc7-116">FILETIME</span><span class="sxs-lookup"><span data-stu-id="5bdc7-116">FILETIME</span></span>](filetime.md)
  
[<span data-ttu-id="5bdc7-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5bdc7-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5bdc7-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5bdc7-118">MAPI Structures</span></span>](mapi-structures.md)


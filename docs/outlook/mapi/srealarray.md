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
ms.openlocfilehash: c64e9a7497a70ea34dc09a5749dd281a24f9413d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770484"
---
# <a name="srealarray"></a><span data-ttu-id="16b27-103">SRealArray</span><span class="sxs-lookup"><span data-stu-id="16b27-103">SRealArray</span></span>

  
  
<span data-ttu-id="16b27-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16b27-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16b27-105">Contém uma matriz de valores float que são usadas para descrever uma propriedade do tipo PT_MV_R4.</span><span class="sxs-lookup"><span data-stu-id="16b27-105">Contains an array of float values that are used to describe a property of type PT_MV_R4.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16b27-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="16b27-106">Header file:</span></span>  <br/> |<span data-ttu-id="16b27-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16b27-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a><span data-ttu-id="16b27-108">Members</span><span class="sxs-lookup"><span data-stu-id="16b27-108">Members</span></span>

 <span data-ttu-id="16b27-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="16b27-109">**cValues**</span></span>
  
> <span data-ttu-id="16b27-110">Contagem de valores na matriz apontado pelo membro **lpflt** .</span><span class="sxs-lookup"><span data-stu-id="16b27-110">Count of values in the array pointed to by the **lpflt** member.</span></span> 
    
 <span data-ttu-id="16b27-111">**lpflt**</span><span class="sxs-lookup"><span data-stu-id="16b27-111">**lpflt**</span></span>
  
> <span data-ttu-id="16b27-112">Ponteiro para uma matriz de valores float.</span><span class="sxs-lookup"><span data-stu-id="16b27-112">Pointer to an array of float values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16b27-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="16b27-113">Remarks</span></span>

<span data-ttu-id="16b27-114">Para obter mais informações sobre o tipo de propriedade PT_MV_R4, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="16b27-114">For more information about the PT_MV_R4 property type, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16b27-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="16b27-115">See also</span></span>



[<span data-ttu-id="16b27-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="16b27-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="16b27-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="16b27-117">MAPI Structures</span></span>](mapi-structures.md)


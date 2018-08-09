---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c207b1db6a24cc60967735e2f4b1a4aa97007750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770435"
---
# <a name="slongarray"></a><span data-ttu-id="f0c45-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="f0c45-103">SLongArray</span></span>

  
  
<span data-ttu-id="f0c45-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0c45-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0c45-105">Contém uma matriz de tipos de valor longo que são usados para descrever uma propriedade do tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="f0c45-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0c45-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f0c45-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0c45-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0c45-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="f0c45-108">Members</span><span class="sxs-lookup"><span data-stu-id="f0c45-108">Members</span></span>

 <span data-ttu-id="f0c45-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f0c45-109">**cValues**</span></span>
  
> <span data-ttu-id="f0c45-110">Contagem de valores na matriz apontado pelo membro **lpl** .</span><span class="sxs-lookup"><span data-stu-id="f0c45-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="f0c45-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="f0c45-111">**lpl**</span></span>
  
> <span data-ttu-id="f0c45-112">Ponteiro para uma matriz de valores longos.</span><span class="sxs-lookup"><span data-stu-id="f0c45-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0c45-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0c45-113">Remarks</span></span>

<span data-ttu-id="f0c45-114">Para obter mais informações sobre PT_MV_LONG, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0c45-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0c45-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0c45-115">See also</span></span>



[<span data-ttu-id="f0c45-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f0c45-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f0c45-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="f0c45-117">MAPI Structures</span></span>](mapi-structures.md)

---
title: SDoubleArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDoubleArray
api_type:
- COM
ms.assetid: b63b26de-faf9-453c-ab8b-fb703ed09ae8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cde59b73381458533910dc8f0a728cc4e6ca0c01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770345"
---
# <a name="sdoublearray"></a><span data-ttu-id="baf83-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="baf83-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="baf83-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="baf83-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="baf83-105">Contém uma matriz de valores duplos usados para descrever uma propriedade do tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="baf83-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="baf83-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="baf83-106">Header file:</span></span>  <br/> |<span data-ttu-id="baf83-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="baf83-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="baf83-108">Members</span><span class="sxs-lookup"><span data-stu-id="baf83-108">Members</span></span>

 <span data-ttu-id="baf83-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="baf83-109">**cValues**</span></span>
  
> <span data-ttu-id="baf83-110">Contagem de valores na matriz apontado pelo membro **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="baf83-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="baf83-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="baf83-111">**lpdbl**</span></span>
  
> <span data-ttu-id="baf83-112">Ponteiro para uma matriz de valores duplos.</span><span class="sxs-lookup"><span data-stu-id="baf83-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="baf83-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="baf83-113">Remarks</span></span>

<span data-ttu-id="baf83-114">Para obter mais informações sobre PT_MV_DOUBLE, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="baf83-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="baf83-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="baf83-115">See also</span></span>



[<span data-ttu-id="baf83-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="baf83-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="baf83-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="baf83-117">MAPI Structures</span></span>](mapi-structures.md)


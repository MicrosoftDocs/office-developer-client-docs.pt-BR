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
ms.openlocfilehash: 6986ed7c9ab9932c5d95fcfb7f74f80088f21971
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580366"
---
# <a name="sdoublearray"></a><span data-ttu-id="35b94-103">SDoubleArray</span><span class="sxs-lookup"><span data-stu-id="35b94-103">SDoubleArray</span></span>

  
  
<span data-ttu-id="35b94-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35b94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35b94-105">Contém uma matriz de valores duplos usados para descrever uma propriedade do tipo PT_MV_DOUBLE.</span><span class="sxs-lookup"><span data-stu-id="35b94-105">Contains an array of doubles used to describe a property of type PT_MV_DOUBLE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35b94-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="35b94-106">Header file:</span></span>  <br/> |<span data-ttu-id="35b94-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35b94-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SDoubleArray
{
  ULONG cValues;
  double FAR *lpdbl;
} SDoubleArray;

```

## <a name="members"></a><span data-ttu-id="35b94-108">Members</span><span class="sxs-lookup"><span data-stu-id="35b94-108">Members</span></span>

 <span data-ttu-id="35b94-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="35b94-109">**cValues**</span></span>
  
> <span data-ttu-id="35b94-110">Contagem de valores na matriz apontado pelo membro **lpdbl** .</span><span class="sxs-lookup"><span data-stu-id="35b94-110">Count of values in the array pointed to by the **lpdbl** member.</span></span> 
    
 <span data-ttu-id="35b94-111">**lpdbl**</span><span class="sxs-lookup"><span data-stu-id="35b94-111">**lpdbl**</span></span>
  
> <span data-ttu-id="35b94-112">Ponteiro para uma matriz de valores duplos.</span><span class="sxs-lookup"><span data-stu-id="35b94-112">Pointer to an array of double values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35b94-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="35b94-113">Remarks</span></span>

<span data-ttu-id="35b94-114">Para obter mais informações sobre PT_MV_DOUBLE, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="35b94-114">For more information about PT_MV_DOUBLE, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35b94-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="35b94-115">See also</span></span>



[<span data-ttu-id="35b94-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="35b94-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="35b94-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="35b94-117">MAPI Structures</span></span>](mapi-structures.md)


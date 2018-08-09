---
title: SLPSTRArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLPSTRArray
api_type:
- COM
ms.assetid: 5f570d9b-eb3d-4fc7-bcbe-348a0b8fe9e9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d2bb6bdb934e0b02831b813b1246a3df4193e0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770441"
---
# <a name="slpstrarray"></a><span data-ttu-id="f05cb-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="f05cb-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="f05cb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f05cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f05cb-105">Contém uma matriz de valores de cadeia de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="f05cb-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f05cb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f05cb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f05cb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f05cb-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="f05cb-108">Members</span><span class="sxs-lookup"><span data-stu-id="f05cb-108">Members</span></span>

 <span data-ttu-id="f05cb-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f05cb-109">**cValues**</span></span>
  
> <span data-ttu-id="f05cb-110">Contagem de valores na matriz apontado pelo membro **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="f05cb-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="f05cb-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="f05cb-111">**lppszA**</span></span>
  
> <span data-ttu-id="f05cb-112">Ponteiro para uma matriz de cadeias de caracteres de 8 bits terminou de null.</span><span class="sxs-lookup"><span data-stu-id="f05cb-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f05cb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f05cb-113">Remarks</span></span>

<span data-ttu-id="f05cb-114">Para obter mais informações sobre PT_MV_STRING8, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f05cb-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f05cb-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f05cb-115">See also</span></span>



[<span data-ttu-id="f05cb-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f05cb-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f05cb-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="f05cb-117">MAPI Structures</span></span>](mapi-structures.md)


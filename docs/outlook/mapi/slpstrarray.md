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
ms.openlocfilehash: 987020bd6fd49fcba9453075cd502bd5cea4c3a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361149"
---
# <a name="slpstrarray"></a><span data-ttu-id="c263b-103">SLPSTRArray</span><span class="sxs-lookup"><span data-stu-id="c263b-103">SLPSTRArray</span></span>

  
  
<span data-ttu-id="c263b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c263b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c263b-105">Contém uma matriz de valores de cadeia de caracteres que são usados para descrever uma propriedade do tipo PT_MV_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c263b-105">Contains an array of string values that are used to describe a property of type PT_MV_STRING8.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c263b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c263b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c263b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c263b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLPSTRArray
{
  ULONG cValues;
  LPSTR FAR *lppszA;
} SLPSTRArray;

```

## <a name="members"></a><span data-ttu-id="c263b-108">Members</span><span class="sxs-lookup"><span data-stu-id="c263b-108">Members</span></span>

 <span data-ttu-id="c263b-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="c263b-109">**cValues**</span></span>
  
> <span data-ttu-id="c263b-110">Contagem de valores na matriz apontada pelo membro **lppszA** .</span><span class="sxs-lookup"><span data-stu-id="c263b-110">Count of values in the array pointed to by the **lppszA** member.</span></span> 
    
 <span data-ttu-id="c263b-111">**lppszA**</span><span class="sxs-lookup"><span data-stu-id="c263b-111">**lppszA**</span></span>
  
> <span data-ttu-id="c263b-112">Ponteiro para uma matriz de cadeias de caracteres de 8 bits finalizadas por nulo.</span><span class="sxs-lookup"><span data-stu-id="c263b-112">Pointer to an array of null-ended 8-bit character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c263b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c263b-113">Remarks</span></span>

<span data-ttu-id="c263b-114">Para obter mais informações sobre o PT_MV_STRING8, confira [lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="c263b-114">For more information about PT_MV_STRING8, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c263b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c263b-115">See also</span></span>



[<span data-ttu-id="c263b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c263b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="c263b-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c263b-117">MAPI Structures</span></span>](mapi-structures.md)


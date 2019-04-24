---
title: SShortArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SShortArray
api_type:
- COM
ms.assetid: 201ceb76-41bc-4d7b-835d-5196bf3dc234
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344496"
---
# <a name="sshortarray"></a><span data-ttu-id="0aa2f-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="0aa2f-103">SShortArray</span></span>

  
  
<span data-ttu-id="0aa2f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa2f-105">Contém uma matriz de valores inteiros não assinados que são usados para descrever uma propriedade do tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="0aa2f-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0aa2f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0aa2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0aa2f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0aa2f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="0aa2f-108">Members</span><span class="sxs-lookup"><span data-stu-id="0aa2f-108">Members</span></span>

 <span data-ttu-id="0aa2f-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0aa2f-109">**cValues**</span></span>
  
> <span data-ttu-id="0aa2f-110">Contagem de valores na matriz apontada pelo membro **LPI** .</span><span class="sxs-lookup"><span data-stu-id="0aa2f-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="0aa2f-111">**LPI**</span><span class="sxs-lookup"><span data-stu-id="0aa2f-111">**lpi**</span></span>
  
> <span data-ttu-id="0aa2f-112">Ponteiro para uma matriz de valores inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="0aa2f-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aa2f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0aa2f-113">Remarks</span></span>

<span data-ttu-id="0aa2f-114">Para obter mais informações sobre o PT_MV_SHORT e outros tipos de propriedade, consulte [tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0aa2f-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aa2f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0aa2f-115">See also</span></span>



[<span data-ttu-id="0aa2f-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0aa2f-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0aa2f-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0aa2f-117">MAPI Structures</span></span>](mapi-structures.md)


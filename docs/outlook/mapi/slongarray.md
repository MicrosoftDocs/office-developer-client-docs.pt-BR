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
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361163"
---
# <a name="slongarray"></a><span data-ttu-id="5c014-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="5c014-103">SLongArray</span></span>

  
  
<span data-ttu-id="5c014-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c014-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c014-105">Contém uma matriz de tipos de valor longo que são usados para descrever uma propriedade do tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="5c014-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c014-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5c014-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c014-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5c014-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="5c014-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c014-108">Members</span></span>

 <span data-ttu-id="5c014-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="5c014-109">**cValues**</span></span>
  
> <span data-ttu-id="5c014-110">Contagem de valores na matriz apontada pelo membro **LPL** .</span><span class="sxs-lookup"><span data-stu-id="5c014-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="5c014-111">**LPL**</span><span class="sxs-lookup"><span data-stu-id="5c014-111">**lpl**</span></span>
  
> <span data-ttu-id="5c014-112">Ponteiro para uma matriz de valores LONG.</span><span class="sxs-lookup"><span data-stu-id="5c014-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5c014-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c014-113">Remarks</span></span>

<span data-ttu-id="5c014-114">Para obter mais informações sobre o PT_MV_LONG, confira [lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5c014-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5c014-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c014-115">See also</span></span>



[<span data-ttu-id="5c014-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5c014-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="5c014-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5c014-117">MAPI Structures</span></span>](mapi-structures.md)


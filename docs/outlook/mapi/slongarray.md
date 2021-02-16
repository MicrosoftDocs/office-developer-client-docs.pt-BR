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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414526"
---
# <a name="slongarray"></a><span data-ttu-id="4569c-103">SLongArray</span><span class="sxs-lookup"><span data-stu-id="4569c-103">SLongArray</span></span>

  
  
<span data-ttu-id="4569c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4569c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4569c-105">Contém uma matriz de tipos de valor LONG que são usados para descrever uma propriedade do tipo PT_MV_LONG.</span><span class="sxs-lookup"><span data-stu-id="4569c-105">Contains an array of LONG value types that are used to describe a property of type PT_MV_LONG.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4569c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4569c-106">Header file:</span></span>  <br/> |<span data-ttu-id="4569c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4569c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a><span data-ttu-id="4569c-108">Members</span><span class="sxs-lookup"><span data-stu-id="4569c-108">Members</span></span>

 <span data-ttu-id="4569c-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="4569c-109">**cValues**</span></span>
  
> <span data-ttu-id="4569c-110">Contagem de valores na matriz apontada pelo membro **lpl.**</span><span class="sxs-lookup"><span data-stu-id="4569c-110">Count of values in the array pointed to by the **lpl** member.</span></span> 
    
 <span data-ttu-id="4569c-111">**lpl**</span><span class="sxs-lookup"><span data-stu-id="4569c-111">**lpl**</span></span>
  
> <span data-ttu-id="4569c-112">Ponteiro para uma matriz de valores LONG.</span><span class="sxs-lookup"><span data-stu-id="4569c-112">Pointer to an array of LONG values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4569c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4569c-113">Remarks</span></span>

<span data-ttu-id="4569c-114">Para obter mais informações sobre PT_MV_LONG, consulte [Lista de tipos de propriedade.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="4569c-114">For more information about PT_MV_LONG, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4569c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="4569c-115">See also</span></span>



[<span data-ttu-id="4569c-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="4569c-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="4569c-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="4569c-117">MAPI Structures</span></span>](mapi-structures.md)


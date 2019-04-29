---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413602"
---
# <a name="swstringarray"></a><span data-ttu-id="17e3b-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="17e3b-103">SWStringArray</span></span>

  
  
<span data-ttu-id="17e3b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17e3b-105">Contém uma matriz de cadeias de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="17e3b-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="17e3b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="17e3b-106">Header file:</span></span>  <br/> |<span data-ttu-id="17e3b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="17e3b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="17e3b-108">Members</span><span class="sxs-lookup"><span data-stu-id="17e3b-108">Members</span></span>

 <span data-ttu-id="17e3b-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="17e3b-109">**cValues**</span></span>
  
> <span data-ttu-id="17e3b-110">Contagem de cadeias de caracteres na matriz apontada pelo membro **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="17e3b-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="17e3b-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="17e3b-111">**lppszW**</span></span>
  
> <span data-ttu-id="17e3b-112">Ponteiro para uma matriz de cadeias de caracteres Unicode de término nulo.</span><span class="sxs-lookup"><span data-stu-id="17e3b-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17e3b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="17e3b-113">Remarks</span></span>

<span data-ttu-id="17e3b-114">Para obter mais informações sobre o PT_MV_UNICODE, consulte [tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="17e3b-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17e3b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="17e3b-115">See also</span></span>



[<span data-ttu-id="17e3b-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="17e3b-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="17e3b-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="17e3b-117">MAPI Structures</span></span>](mapi-structures.md)


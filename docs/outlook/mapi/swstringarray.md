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
ms.openlocfilehash: 1578e26ec96f69975c2304cb185f352193a52c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770553"
---
# <a name="swstringarray"></a><span data-ttu-id="2d680-103">SWStringArray</span><span class="sxs-lookup"><span data-stu-id="2d680-103">SWStringArray</span></span>

  
  
<span data-ttu-id="2d680-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d680-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d680-105">Contém uma matriz de cadeias de caracteres que são usadas para descrever uma propriedade do tipo PT_MV_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2d680-105">Contains an array of character strings that are used to describe a property of type PT_MV_UNICODE.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d680-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2d680-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d680-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d680-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a><span data-ttu-id="2d680-108">Members</span><span class="sxs-lookup"><span data-stu-id="2d680-108">Members</span></span>

 <span data-ttu-id="2d680-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="2d680-109">**cValues**</span></span>
  
> <span data-ttu-id="2d680-110">Contagem de cadeias de caracteres na matriz apontado pelo membro **lppszW** .</span><span class="sxs-lookup"><span data-stu-id="2d680-110">Count of strings in the array pointed to by the **lppszW** member.</span></span> 
    
 <span data-ttu-id="2d680-111">**lppszW**</span><span class="sxs-lookup"><span data-stu-id="2d680-111">**lppszW**</span></span>
  
> <span data-ttu-id="2d680-112">Ponteiro para uma matriz de cadeias de caracteres Unicode null-encerrada.</span><span class="sxs-lookup"><span data-stu-id="2d680-112">Pointer to an array of null-ended Unicode character strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d680-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d680-113">Remarks</span></span>

<span data-ttu-id="2d680-114">Para obter mais informações sobre PT_MV_UNICODE, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="2d680-114">For more information about PT_MV_UNICODE, see [Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d680-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d680-115">See also</span></span>



[<span data-ttu-id="2d680-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="2d680-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="2d680-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="2d680-117">MAPI Structures</span></span>](mapi-structures.md)


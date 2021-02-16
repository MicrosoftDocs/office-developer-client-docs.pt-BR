---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438285"
---
# <a name="sbinaryarray"></a><span data-ttu-id="6b642-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="6b642-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="6b642-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b642-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b642-105">Contém uma matriz de valores binários.</span><span class="sxs-lookup"><span data-stu-id="6b642-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b642-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6b642-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b642-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b642-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="6b642-108">Members</span><span class="sxs-lookup"><span data-stu-id="6b642-108">Members</span></span>

 <span data-ttu-id="6b642-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="6b642-109">**cValues**</span></span>
  
> <span data-ttu-id="6b642-110">Contagem de valores na matriz apontada pelo membro **lpbin.**</span><span class="sxs-lookup"><span data-stu-id="6b642-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="6b642-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="6b642-111">**lpbin**</span></span>
  
> <span data-ttu-id="6b642-112">Ponteiro para uma matriz de [estruturas SBinary](sbinary.md) que contém os valores binários.</span><span class="sxs-lookup"><span data-stu-id="6b642-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b642-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b642-113">Remarks</span></span>

<span data-ttu-id="6b642-114">A **estrutura SBinaryArray** é usada para descrever propriedades do tipo PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="6b642-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="6b642-115">Para obter mais informações sobre PT_MV_BINARY, consulte [Lista de tipos de propriedade.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="6b642-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b642-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b642-116">See also</span></span>



[<span data-ttu-id="6b642-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="6b642-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="6b642-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b642-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="6b642-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="6b642-119">MAPI Structures</span></span>](mapi-structures.md)


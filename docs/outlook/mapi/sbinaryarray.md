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
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770294"
---
# <a name="sbinaryarray"></a><span data-ttu-id="857dd-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="857dd-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="857dd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="857dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="857dd-105">Contém uma matriz de valores binários.</span><span class="sxs-lookup"><span data-stu-id="857dd-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="857dd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="857dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="857dd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="857dd-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="857dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="857dd-108">Members</span></span>

 <span data-ttu-id="857dd-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="857dd-109">**cValues**</span></span>
  
> <span data-ttu-id="857dd-110">Contagem de valores na matriz apontado pelo membro **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="857dd-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="857dd-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="857dd-111">**lpbin**</span></span>
  
> <span data-ttu-id="857dd-112">Ponteiro para uma matriz de estruturas de [SBinary](sbinary.md) que contém os valores binários.</span><span class="sxs-lookup"><span data-stu-id="857dd-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="857dd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="857dd-113">Remarks</span></span>

<span data-ttu-id="857dd-114">A estrutura **SBinaryArray** é usada para descrever as propriedades do tipo PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="857dd-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="857dd-115">Para obter mais informações sobre PT_MV_BINARY, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="857dd-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="857dd-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="857dd-116">See also</span></span>



[<span data-ttu-id="857dd-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="857dd-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="857dd-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="857dd-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="857dd-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="857dd-119">MAPI Structures</span></span>](mapi-structures.md)


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
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586463"
---
# <a name="sbinaryarray"></a><span data-ttu-id="84645-103">SBinaryArray</span><span class="sxs-lookup"><span data-stu-id="84645-103">SBinaryArray</span></span>

  
  
<span data-ttu-id="84645-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84645-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84645-105">Contém uma matriz de valores binários.</span><span class="sxs-lookup"><span data-stu-id="84645-105">Contains an array of binary values.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84645-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="84645-106">Header file:</span></span>  <br/> |<span data-ttu-id="84645-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84645-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a><span data-ttu-id="84645-108">Members</span><span class="sxs-lookup"><span data-stu-id="84645-108">Members</span></span>

 <span data-ttu-id="84645-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="84645-109">**cValues**</span></span>
  
> <span data-ttu-id="84645-110">Contagem de valores na matriz apontado pelo membro **lpbin** .</span><span class="sxs-lookup"><span data-stu-id="84645-110">Count of values in the array pointed to by the **lpbin** member.</span></span> 
    
 <span data-ttu-id="84645-111">**lpbin**</span><span class="sxs-lookup"><span data-stu-id="84645-111">**lpbin**</span></span>
  
> <span data-ttu-id="84645-112">Ponteiro para uma matriz de estruturas de [SBinary](sbinary.md) que contém os valores binários.</span><span class="sxs-lookup"><span data-stu-id="84645-112">Pointer to an array of [SBinary](sbinary.md) structures that holds the binary values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="84645-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="84645-113">Remarks</span></span>

<span data-ttu-id="84645-114">A estrutura **SBinaryArray** é usada para descrever as propriedades do tipo PT_MV_BINARY.</span><span class="sxs-lookup"><span data-stu-id="84645-114">The **SBinaryArray** structure is used to describe properties of type PT_MV_BINARY.</span></span> 
  
<span data-ttu-id="84645-115">Para obter mais informações sobre PT_MV_BINARY, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="84645-115">For more information about PT_MV_BINARY, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84645-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="84645-116">See also</span></span>



[<span data-ttu-id="84645-117">SBinary</span><span class="sxs-lookup"><span data-stu-id="84645-117">SBinary</span></span>](sbinary.md)
  
[<span data-ttu-id="84645-118">SPropValue</span><span class="sxs-lookup"><span data-stu-id="84645-118">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="84645-119">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="84645-119">MAPI Structures</span></span>](mapi-structures.md)


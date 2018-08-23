---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 29b26996bc337045489758a14857a30fafe48e54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576432"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="d1e7e-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="d1e7e-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="d1e7e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1e7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1e7e-105">Contém uma matriz de estruturas [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) que são usadas para descrever uma propriedade do tipo PT_MV_I8.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-105">Contains an array of [LARGE_INTEGER](http://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1e7e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d1e7e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d1e7e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1e7e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="d1e7e-108">Members</span><span class="sxs-lookup"><span data-stu-id="d1e7e-108">Members</span></span>

 <span data-ttu-id="d1e7e-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="d1e7e-109">**cValues**</span></span>
  
> <span data-ttu-id="d1e7e-110">Contagem de valores na matriz apontado pelo membro **lpli** .</span><span class="sxs-lookup"><span data-stu-id="d1e7e-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="d1e7e-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="d1e7e-111">**lpli**</span></span>
  
> <span data-ttu-id="d1e7e-112">Ponteiro para uma matriz de estruturas **LARGE_INTEGER** reter os valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="d1e7e-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d1e7e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e7e-113">Remarks</span></span>

<span data-ttu-id="d1e7e-114">Para obter mais informações sobre PT_MV_18, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="d1e7e-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1e7e-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e7e-115">See also</span></span>



[<span data-ttu-id="d1e7e-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d1e7e-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="d1e7e-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="d1e7e-117">MAPI Structures</span></span>](mapi-structures.md)


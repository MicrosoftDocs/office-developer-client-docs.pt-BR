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
ms.openlocfilehash: b684309211bbc008856311158c67864d958c96a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573030"
---
# <a name="sshortarray"></a><span data-ttu-id="f9786-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="f9786-103">SShortArray</span></span>

  
  
<span data-ttu-id="f9786-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9786-105">Contém uma matriz de valores de inteiro não assinado que são usadas para descrever uma propriedade do tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="f9786-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9786-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f9786-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9786-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9786-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="f9786-108">Members</span><span class="sxs-lookup"><span data-stu-id="f9786-108">Members</span></span>

 <span data-ttu-id="f9786-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f9786-109">**cValues**</span></span>
  
> <span data-ttu-id="f9786-110">Contagem de valores na matriz apontado pelo membro **lpi** .</span><span class="sxs-lookup"><span data-stu-id="f9786-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="f9786-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="f9786-111">**lpi**</span></span>
  
> <span data-ttu-id="f9786-112">Ponteiro para uma matriz de valores de inteiro não assinado.</span><span class="sxs-lookup"><span data-stu-id="f9786-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9786-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9786-113">Remarks</span></span>

<span data-ttu-id="f9786-114">Para obter mais informações sobre PT_MV_SHORT e outros tipos de propriedade, consulte [Tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f9786-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9786-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9786-115">See also</span></span>



[<span data-ttu-id="f9786-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f9786-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f9786-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="f9786-117">MAPI Structures</span></span>](mapi-structures.md)


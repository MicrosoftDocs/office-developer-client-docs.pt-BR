---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430382"
---
# <a name="sapptimearray"></a><span data-ttu-id="f35d4-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="f35d4-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="f35d4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f35d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f35d4-105">Contém uma matriz de valores de tempo.</span><span class="sxs-lookup"><span data-stu-id="f35d4-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f35d4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f35d4-106">Header file:</span></span>  <br/> |<span data-ttu-id="f35d4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f35d4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="f35d4-108">Members</span><span class="sxs-lookup"><span data-stu-id="f35d4-108">Members</span></span>

 <span data-ttu-id="f35d4-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f35d4-109">**cValues**</span></span>
  
> <span data-ttu-id="f35d4-110">Contagem de valores na matriz apontada pelo membro **lpat** .</span><span class="sxs-lookup"><span data-stu-id="f35d4-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="f35d4-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="f35d4-111">**lpat**</span></span>
  
> <span data-ttu-id="f35d4-112">Ponteiro para uma matriz de valores de tempo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f35d4-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f35d4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f35d4-113">Remarks</span></span>

<span data-ttu-id="f35d4-114">A estrutura **SAppTimeArray** é usada para definir propriedades do tipo PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="f35d4-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="f35d4-115">Para obter mais informações sobre o PT_MV_APPTIME, confira [lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="f35d4-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f35d4-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="f35d4-116">See also</span></span>



[<span data-ttu-id="f35d4-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="f35d4-117">MAPI Structures</span></span>](mapi-structures.md)


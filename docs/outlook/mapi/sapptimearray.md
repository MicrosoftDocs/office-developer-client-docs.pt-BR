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
ms.openlocfilehash: 834a7141f0e7150140fa27c21d88db422d6f5561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770286"
---
# <a name="sapptimearray"></a><span data-ttu-id="0e82e-103">SAppTimeArray</span><span class="sxs-lookup"><span data-stu-id="0e82e-103">SAppTimeArray</span></span>

  
  
<span data-ttu-id="0e82e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e82e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e82e-105">Contém uma matriz de valores de tempo.</span><span class="sxs-lookup"><span data-stu-id="0e82e-105">Contains an array of time values.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e82e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0e82e-106">Header file:</span></span>  <br/> |<span data-ttu-id="0e82e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e82e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a><span data-ttu-id="0e82e-108">Members</span><span class="sxs-lookup"><span data-stu-id="0e82e-108">Members</span></span>

 <span data-ttu-id="0e82e-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="0e82e-109">**cValues**</span></span>
  
> <span data-ttu-id="0e82e-110">Contagem de valores na matriz apontado pelo membro **lpat** .</span><span class="sxs-lookup"><span data-stu-id="0e82e-110">Count of values in the array pointed to by the **lpat** member.</span></span> 
    
 <span data-ttu-id="0e82e-111">**lpat**</span><span class="sxs-lookup"><span data-stu-id="0e82e-111">**lpat**</span></span>
  
> <span data-ttu-id="0e82e-112">Ponteiro para uma matriz de valores de tempo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e82e-112">Pointer to an array of application time values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0e82e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e82e-113">Remarks</span></span>

<span data-ttu-id="0e82e-114">A estrutura **SAppTimeArray** é usada para definir as propriedades do tipo PT_MV_APPTIME.</span><span class="sxs-lookup"><span data-stu-id="0e82e-114">The **SAppTimeArray** structure is used to define properties of type PT_MV_APPTIME.</span></span> <span data-ttu-id="0e82e-115">Para obter mais informações sobre PT_MV_APPTIME, consulte a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="0e82e-115">For more information about PT_MV_APPTIME, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0e82e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e82e-116">See also</span></span>



[<span data-ttu-id="0e82e-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0e82e-117">MAPI Structures</span></span>](mapi-structures.md)


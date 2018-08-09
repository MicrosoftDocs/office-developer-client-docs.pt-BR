---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770291"
---
# <a name="sbinary"></a><span data-ttu-id="0a0ed-103">SBinary</span><span class="sxs-lookup"><span data-stu-id="0a0ed-103">SBinary</span></span>

  
  
<span data-ttu-id="0a0ed-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a0ed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a0ed-105">Descreve uma propriedade do tipo PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="0a0ed-105">Describes a property of type PT_BINARY.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a0ed-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0a0ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a0ed-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a0ed-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a><span data-ttu-id="0a0ed-108">Members</span><span class="sxs-lookup"><span data-stu-id="0a0ed-108">Members</span></span>

 <span data-ttu-id="0a0ed-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="0a0ed-109">**cb**</span></span>
  
> <span data-ttu-id="0a0ed-110">Contagem de bytes no membro **lpb** .</span><span class="sxs-lookup"><span data-stu-id="0a0ed-110">Count of bytes in the **lpb** member.</span></span> 
    
 <span data-ttu-id="0a0ed-111">**lpb**</span><span class="sxs-lookup"><span data-stu-id="0a0ed-111">**lpb**</span></span>
  
> <span data-ttu-id="0a0ed-112">Ponteiro para o valor da propriedade PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="0a0ed-112">Pointer to the PT_BINARY property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a0ed-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a0ed-113">Remarks</span></span>

<span data-ttu-id="0a0ed-114">Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a0ed-114">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a0ed-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a0ed-115">See also</span></span>



[<span data-ttu-id="0a0ed-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0a0ed-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0a0ed-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0a0ed-117">MAPI Structures</span></span>](mapi-structures.md)


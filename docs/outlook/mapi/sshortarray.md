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
ms.openlocfilehash: 8ea7d51b15a6e6acd44a3c0b6158378661f311bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429611"
---
# <a name="sshortarray"></a><span data-ttu-id="eaf66-103">SShortArray</span><span class="sxs-lookup"><span data-stu-id="eaf66-103">SShortArray</span></span>

  
  
<span data-ttu-id="eaf66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eaf66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eaf66-105">Contém uma matriz de valores inteiros não assinados que são usados para descrever uma propriedade do tipo PT_MV_SHORT.</span><span class="sxs-lookup"><span data-stu-id="eaf66-105">Contains an array of unsigned integer values that are used to describe a property of type PT_MV_SHORT.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eaf66-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eaf66-106">Header file:</span></span>  <br/> |<span data-ttu-id="eaf66-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eaf66-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SShortArray
{
  ULONG cValues;
  short int FAR *lpi;
} SShortArray;

```

## <a name="members"></a><span data-ttu-id="eaf66-108">Members</span><span class="sxs-lookup"><span data-stu-id="eaf66-108">Members</span></span>

 <span data-ttu-id="eaf66-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="eaf66-109">**cValues**</span></span>
  
> <span data-ttu-id="eaf66-110">Contagem de valores na matriz apontada pelo **membro lpi.**</span><span class="sxs-lookup"><span data-stu-id="eaf66-110">Count of values in the array pointed to by the **lpi** member.</span></span> 
    
 <span data-ttu-id="eaf66-111">**lpi**</span><span class="sxs-lookup"><span data-stu-id="eaf66-111">**lpi**</span></span>
  
> <span data-ttu-id="eaf66-112">Ponteiro para uma matriz de valores inteiros não assinados.</span><span class="sxs-lookup"><span data-stu-id="eaf66-112">Pointer to an array of unsigned integer values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eaf66-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="eaf66-113">Remarks</span></span>

<span data-ttu-id="eaf66-114">Para obter mais informações sobre PT_MV_SHORT e outros tipos de propriedade, consulte [Tipos de propriedade.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="eaf66-114">For more information about PT_MV_SHORT and other property types, see [Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eaf66-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="eaf66-115">See also</span></span>



[<span data-ttu-id="eaf66-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="eaf66-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="eaf66-117">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="eaf66-117">MAPI Structures</span></span>](mapi-structures.md)


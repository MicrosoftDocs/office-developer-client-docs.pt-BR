---
title: SPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropTagArray
api_type:
- COM
ms.assetid: 4a9e1579-bebe-4a51-8ced-6dba9c3bcb63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a5be98298ab1f9333ac1c223a6ef594e60dd86a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344433"
---
# <a name="sproptagarray"></a><span data-ttu-id="dc970-103">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="dc970-103">SPropTagArray</span></span>

  
  
<span data-ttu-id="dc970-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc970-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc970-105">Contém uma matriz de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dc970-105">Contains an array of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc970-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dc970-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc970-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dc970-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dc970-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="dc970-108">Related macros:</span></span>  <br/> |<span data-ttu-id="dc970-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span><span class="sxs-lookup"><span data-stu-id="dc970-109">[CbNewSPropTagArray](cbnewsproptagarray.md), [CbSPropTagArray](cbsproptagarray.md), [SizedSPropTagArray](sizedsproptagarray.md)</span></span> <br/> |
   
```cpp
typedef struct _SPropTagArray
{
  ULONG cValues;
  ULONG aulPropTag[MAPI_DIM];
} SPropTagArray, FAR *LPSPropTagArray;

```

## <a name="members"></a><span data-ttu-id="dc970-110">Members</span><span class="sxs-lookup"><span data-stu-id="dc970-110">Members</span></span>

 <span data-ttu-id="dc970-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="dc970-111">**cValues**</span></span>
  
> <span data-ttu-id="dc970-112">Contagem de marcas de propriedade na matriz indicada pelo membro **aulPropTag** .</span><span class="sxs-lookup"><span data-stu-id="dc970-112">Count of property tags in the array indicated by the **aulPropTag** member.</span></span> 
    
 <span data-ttu-id="dc970-113">**aulPropTag**</span><span class="sxs-lookup"><span data-stu-id="dc970-113">**aulPropTag**</span></span>
  
> <span data-ttu-id="dc970-114">Matriz de marcas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="dc970-114">Array of property tags.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc970-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc970-115">Remarks</span></span>

<span data-ttu-id="dc970-116">Uma marca de propriedade é um inteiro não assinado de 32 bits que consiste em duas partes:</span><span class="sxs-lookup"><span data-stu-id="dc970-116">A property tag is a 32-bit unsigned integer that consists of two parts:</span></span> 
  
- <span data-ttu-id="dc970-117">Um identificador na ordem alta de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dc970-117">An identifier in the high-order 16 bits.</span></span>
    
- <span data-ttu-id="dc970-118">Um tipo na ordem baixa de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dc970-118">A type in the low-order 16 bits.</span></span>
    
<span data-ttu-id="dc970-119">O identificador é um valor numérico em um intervalo específico.</span><span class="sxs-lookup"><span data-stu-id="dc970-119">The identifier is a numeric value in a particular range.</span></span> <span data-ttu-id="dc970-120">MAPI define intervalos para identificadores para descrever o que a propriedade é usada e quem é responsável por mantê-la.</span><span class="sxs-lookup"><span data-stu-id="dc970-120">MAPI defines ranges for identifiers to describe what the property is used for and who is responsible for maintaining it.</span></span> <span data-ttu-id="dc970-121">MAPI define restrições para cada uma das marcas de propriedade que ele suporta no arquivo de cabeçalho Mapitags. h.</span><span class="sxs-lookup"><span data-stu-id="dc970-121">MAPI defines constraints for each of the property tags that it supports in the Mapitags.h header file.</span></span>
  
<span data-ttu-id="dc970-122">O tipo indica o formato do valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="dc970-122">The type indicates the format for the property's value.</span></span> <span data-ttu-id="dc970-123">MAPI define constantes para cada um dos tipos de propriedade que ele suporta no arquivo de cabeçalho mapidefs. h.</span><span class="sxs-lookup"><span data-stu-id="dc970-123">MAPI defines constants for each of the property types that it supports in the Mapidefs.h header file.</span></span> 
  
<span data-ttu-id="dc970-124">Para obter mais informações sobre marcas de propriedade e seus componentes, consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="dc970-124">For more information about property tags and their components, see one of the following topics:</span></span> 
  
[<span data-ttu-id="dc970-125">Marcas de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="dc970-125">MAPI Property Tags</span></span>](mapi-property-tags.md)
  
[<span data-ttu-id="dc970-126">Visão geral do identificador de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="dc970-126">MAPI Property Identifier Overview</span></span>](mapi-property-identifier-overview.md)
  
[<span data-ttu-id="dc970-127">Visão geral do tipo de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="dc970-127">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)
  
<span data-ttu-id="dc970-128">Para obter uma lista completa dos tipos de propriedade de valor único e múltiplos valores, confira o apêndice, os identificadores de [propriedade e os tipos](property-identifiers-and-types.md).</span><span class="sxs-lookup"><span data-stu-id="dc970-128">For a complete list of the single-valued and multi-valued property types, see the appendix, [Property Identifiers and Types](property-identifiers-and-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc970-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc970-129">See also</span></span>



[<span data-ttu-id="dc970-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="dc970-130">MAPI Structures</span></span>](mapi-structures.md)


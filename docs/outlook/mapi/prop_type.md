---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770176"
---
# <a name="proptype"></a><span data-ttu-id="473c5-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="473c5-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="473c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="473c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="473c5-105">Retorna o tipo de propriedade de uma marca de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="473c5-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="473c5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="473c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="473c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="473c5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="473c5-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="473c5-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="473c5-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="473c5-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="473c5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="473c5-110">Parameters</span></span>

 <span data-ttu-id="473c5-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="473c5-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="473c5-112">Marca de propriedade que contém o tipo de propriedade a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="473c5-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="473c5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="473c5-113">Remarks</span></span>

<span data-ttu-id="473c5-114">A macro **PROP_TYPE** pode ser usada para determinar o tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="473c5-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="473c5-115">Por exemplo, chamando PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resultados no valor PT_BINARY sendo retornados.</span><span class="sxs-lookup"><span data-stu-id="473c5-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="473c5-116">A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits).</span><span class="sxs-lookup"><span data-stu-id="473c5-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="473c5-117">A macro **PROP_TYPE** extrai o tipo de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="473c5-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="473c5-118">Os bits restantes do valor de retorno são definidos com zeros.</span><span class="sxs-lookup"><span data-stu-id="473c5-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="473c5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="473c5-119">See also</span></span>



[<span data-ttu-id="473c5-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="473c5-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="473c5-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="473c5-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


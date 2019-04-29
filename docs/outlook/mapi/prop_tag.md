---
title: PROP_TAG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TAG
api_type:
- COM
ms.assetid: d8c9d18c-4043-41f3-8501-8be8e3a2c9ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7ab4e4e9e51849037a91a071f16294cfdf10870c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425880"
---
# <a name="proptag"></a><span data-ttu-id="08dbe-103">PROP_TAG</span><span class="sxs-lookup"><span data-stu-id="08dbe-103">PROP_TAG</span></span>

<span data-ttu-id="08dbe-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08dbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08dbe-105">Retorna uma marca de propriedade criada combinando um tipo de propriedade especificado e um identificador.</span><span class="sxs-lookup"><span data-stu-id="08dbe-105">Returns a property tag created by combining a specified property type and identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08dbe-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="08dbe-106">Header file:</span></span>  <br/> |<span data-ttu-id="08dbe-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08dbe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="08dbe-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="08dbe-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="08dbe-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="08dbe-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TAG (ulPropType, ulPropID)
```

## <a name="parameters"></a><span data-ttu-id="08dbe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08dbe-110">Parameters</span></span>

<span data-ttu-id="08dbe-111">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="08dbe-111">_ulPropType_</span></span>
  
> <span data-ttu-id="08dbe-112">Tipo de propriedade para a nova marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="08dbe-112">Property type for the new property tag.</span></span>
    
<span data-ttu-id="08dbe-113">_ulPropID_</span><span class="sxs-lookup"><span data-stu-id="08dbe-113">_ulPropID_</span></span>
  
> <span data-ttu-id="08dbe-114">Identificador de propriedade para a nova marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="08dbe-114">Property identifier for the new property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08dbe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="08dbe-115">Remarks</span></span>

<span data-ttu-id="08dbe-116">A macro de **marca prop\_** cria uma marca de propriedade para uma propriedade do tipo _ulPropType_ e o identificador especificado em _ulPropID_.</span><span class="sxs-lookup"><span data-stu-id="08dbe-116">The **PROP\_TAG** macro creates a property tag for a property of type  _ulPropType_ and the identifier that is specified in  _ulPropID_.</span></span> <span data-ttu-id="08dbe-117">Por exemplo, uma marca de propriedade para um identificador de entrada pode ser criada usando a macro **PROP_TAG** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="08dbe-117">For example, a property tag for an entry identifier can be created by using the **PROP_TAG** macro as follows:</span></span> 
  
```cpp
PROP_TAG( PT_BINARY, 0x0FFF)

```

<span data-ttu-id="08dbe-118">Os 16 bits de ordem inferior da marca Property retornada contêm o tipo de propriedade, PT_BINARY e os 16 bits de ordem alta contêm o identificador de propriedade, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="08dbe-118">The low-order 16 bits of the returned property tag contain the property type, PT_BINARY, and the high-order 16 bits contain the property identifier, 0xFFFF.</span></span>
  
<span data-ttu-id="08dbe-119">Para obter mais informações sobre as marcas de propriedade, consulte [MAPI Property Tags](mapi-property-tags.md).</span><span class="sxs-lookup"><span data-stu-id="08dbe-119">For more information about property tags, see [MAPI Property Tags](mapi-property-tags.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="08dbe-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="08dbe-120">See also</span></span>

- [<span data-ttu-id="08dbe-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="08dbe-121">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="08dbe-122">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="08dbe-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)


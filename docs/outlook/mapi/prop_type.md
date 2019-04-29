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
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412832"
---
# <a name="proptype"></a><span data-ttu-id="34801-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="34801-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="34801-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34801-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34801-105">Retorna o tipo de propriedade de uma marca de propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="34801-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34801-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="34801-106">Header file:</span></span>  <br/> |<span data-ttu-id="34801-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="34801-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="34801-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="34801-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="34801-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="34801-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="34801-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34801-110">Parameters</span></span>

 <span data-ttu-id="34801-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="34801-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="34801-112">Marca de propriedade que contém o tipo de propriedade a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="34801-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34801-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34801-113">Remarks</span></span>

<span data-ttu-id="34801-114">A macro **PROP_TYPE** pode ser usada para determinar o tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="34801-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="34801-115">Por exemplo, chamar PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resulta no valor PT_BINARY que está sendo retornado.</span><span class="sxs-lookup"><span data-stu-id="34801-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="34801-116">Cada marca de propriedade contém o tipo de propriedade na palavra de ordem inferior (bits 0 a 15) e o identificador de propriedade na palavra de ordem alta (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="34801-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="34801-117">A macro **PROP_TYPE** extrai o tipo de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="34801-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="34801-118">Os bits restantes do valor de retorno são definidos como zeros.</span><span class="sxs-lookup"><span data-stu-id="34801-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34801-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="34801-119">See also</span></span>



[<span data-ttu-id="34801-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="34801-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="34801-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="34801-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


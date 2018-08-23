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
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571819"
---
# <a name="proptype"></a><span data-ttu-id="25c77-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="25c77-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="25c77-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25c77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25c77-105">Retorna o tipo de propriedade de uma marca de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="25c77-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25c77-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="25c77-106">Header file:</span></span>  <br/> |<span data-ttu-id="25c77-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25c77-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="25c77-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="25c77-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="25c77-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="25c77-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="25c77-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25c77-110">Parameters</span></span>

 <span data-ttu-id="25c77-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="25c77-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="25c77-112">Marca de propriedade que contém o tipo de propriedade a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="25c77-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25c77-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="25c77-113">Remarks</span></span>

<span data-ttu-id="25c77-114">A macro **PROP_TYPE** pode ser usada para determinar o tipo de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="25c77-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="25c77-115">Por exemplo, chamando PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) resultados no valor PT_BINARY sendo retornados.</span><span class="sxs-lookup"><span data-stu-id="25c77-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="25c77-116">A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits).</span><span class="sxs-lookup"><span data-stu-id="25c77-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="25c77-117">A macro **PROP_TYPE** extrai o tipo de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="25c77-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="25c77-118">Os bits restantes do valor de retorno são definidos com zeros.</span><span class="sxs-lookup"><span data-stu-id="25c77-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25c77-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="25c77-119">See also</span></span>



[<span data-ttu-id="25c77-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="25c77-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="25c77-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="25c77-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


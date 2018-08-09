---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad4b9d3f7c2ca1766ecca4fe9467fc49098f2212
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770187"
---
# <a name="propid"></a><span data-ttu-id="3ad21-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="3ad21-103">PROP_ID</span></span>

  
  
<span data-ttu-id="3ad21-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ad21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ad21-105">Retorna o identificador de propriedade de uma marca de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="3ad21-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ad21-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3ad21-106">Header file:</span></span>  <br/> |<span data-ttu-id="3ad21-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ad21-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3ad21-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="3ad21-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="3ad21-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3ad21-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="3ad21-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ad21-110">Parameters</span></span>

 <span data-ttu-id="3ad21-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="3ad21-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="3ad21-112">Marca de propriedade que contém o identificador a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3ad21-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ad21-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ad21-113">Remarks</span></span>

<span data-ttu-id="3ad21-114">A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits).</span><span class="sxs-lookup"><span data-stu-id="3ad21-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="3ad21-115">A macro **PROP_ID** extrai o identificador de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="3ad21-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="3ad21-116">Os bits restantes do valor de retorno são definidos com zeros.</span><span class="sxs-lookup"><span data-stu-id="3ad21-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="3ad21-117">A macro **PROP_ID** pode ser usada, por exemplo, para recuperar um identificador a serem passados para [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="3ad21-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="3ad21-118">**GetNamesFromIDs** recupera o nome da propriedade associado a um identificador para uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="3ad21-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ad21-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ad21-119">See also</span></span>



[<span data-ttu-id="3ad21-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3ad21-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3ad21-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="3ad21-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


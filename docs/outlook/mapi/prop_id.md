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
ms.openlocfilehash: e1846b4be93bf6300ea89a9ae3133fbba82b344e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573121"
---
# <a name="propid"></a><span data-ttu-id="488a9-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="488a9-103">PROP_ID</span></span>

  
  
<span data-ttu-id="488a9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="488a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="488a9-105">Retorna o identificador de propriedade de uma marca de propriedade especificado.</span><span class="sxs-lookup"><span data-stu-id="488a9-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="488a9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="488a9-106">Header file:</span></span>  <br/> |<span data-ttu-id="488a9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="488a9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="488a9-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="488a9-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="488a9-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="488a9-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="488a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="488a9-110">Parameters</span></span>

 <span data-ttu-id="488a9-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="488a9-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="488a9-112">Marca de propriedade que contém o identificador a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="488a9-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="488a9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="488a9-113">Remarks</span></span>

<span data-ttu-id="488a9-114">A marca de cada propriedade contém o tipo de propriedade da palavra de ordem baixa (0 a 15 bits) e o identificador de propriedade da palavra de ordem alta (16 a 31 bits).</span><span class="sxs-lookup"><span data-stu-id="488a9-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="488a9-115">A macro **PROP_ID** extrai o identificador de propriedade e a coloca em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="488a9-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="488a9-116">Os bits restantes do valor de retorno são definidos com zeros.</span><span class="sxs-lookup"><span data-stu-id="488a9-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="488a9-117">A macro **PROP_ID** pode ser usada, por exemplo, para recuperar um identificador a serem passados para [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="488a9-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="488a9-118">**GetNamesFromIDs** recupera o nome da propriedade associado a um identificador para uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="488a9-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="488a9-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="488a9-119">See also</span></span>



[<span data-ttu-id="488a9-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="488a9-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="488a9-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="488a9-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


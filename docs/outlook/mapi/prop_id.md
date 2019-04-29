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
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409129"
---
# <a name="propid"></a><span data-ttu-id="23c70-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="23c70-103">PROP_ID</span></span>

  
  
<span data-ttu-id="23c70-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23c70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23c70-105">Retorna o identificador de propriedade de uma marca de propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="23c70-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23c70-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="23c70-106">Header file:</span></span>  <br/> |<span data-ttu-id="23c70-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="23c70-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="23c70-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="23c70-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="23c70-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="23c70-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="23c70-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23c70-110">Parameters</span></span>

 <span data-ttu-id="23c70-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="23c70-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="23c70-112">Marca de propriedade que contém o identificador a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="23c70-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23c70-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="23c70-113">Remarks</span></span>

<span data-ttu-id="23c70-114">Cada marca de propriedade contém o tipo de propriedade na palavra de ordem inferior (bits 0 a 15) e o identificador de propriedade na palavra de ordem alta (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="23c70-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="23c70-115">A macro **PROP_ID** extrai o identificador de propriedade e coloca-o em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="23c70-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="23c70-116">Os bits restantes do valor de retorno são definidos como zeros.</span><span class="sxs-lookup"><span data-stu-id="23c70-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="23c70-117">A macro **PROP_ID** pode ser usada, por exemplo, para recuperar um identificador para passar para o [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="23c70-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="23c70-118">**GetNamesFromIDs** recupera o nome da propriedade associada a um identificador de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="23c70-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="23c70-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="23c70-119">See also</span></span>



[<span data-ttu-id="23c70-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="23c70-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="23c70-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="23c70-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


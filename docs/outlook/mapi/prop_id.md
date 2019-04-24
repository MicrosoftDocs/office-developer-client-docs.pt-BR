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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328571"
---
# <a name="propid"></a><span data-ttu-id="46714-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="46714-103">PROP_ID</span></span>

  
  
<span data-ttu-id="46714-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46714-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46714-105">Retorna o identificador de propriedade de uma marca de propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="46714-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46714-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="46714-106">Header file:</span></span>  <br/> |<span data-ttu-id="46714-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="46714-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="46714-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="46714-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="46714-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="46714-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="46714-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46714-110">Parameters</span></span>

 <span data-ttu-id="46714-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="46714-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="46714-112">Marca de propriedade que contém o identificador a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="46714-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46714-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="46714-113">Remarks</span></span>

<span data-ttu-id="46714-114">Cada marca de propriedade contém o tipo de propriedade na palavra de ordem inferior (bits 0 a 15) e o identificador de propriedade na palavra de ordem alta (bits 16 a 31).</span><span class="sxs-lookup"><span data-stu-id="46714-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="46714-115">A macro **PROP_ID** extrai o identificador de propriedade e coloca-o em bits 0 a 15 do inteiro a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="46714-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="46714-116">Os bits restantes do valor de retorno são definidos como zeros.</span><span class="sxs-lookup"><span data-stu-id="46714-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="46714-117">A macro **PROP_ID** pode ser usada, por exemplo, para recuperar um identificador para passar para o [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="46714-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="46714-118">**GetNamesFromIDs** recupera o nome da propriedade associada a um identificador de uma propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="46714-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46714-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="46714-119">See also</span></span>



[<span data-ttu-id="46714-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="46714-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="46714-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="46714-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)


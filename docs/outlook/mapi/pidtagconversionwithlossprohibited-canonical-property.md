---
title: Propriedade canônica PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417123"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="c9ba4-103">Propriedade canônica PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="c9ba4-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="c9ba4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9ba4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9ba4-105">Contém TRUE se um agente de transferência de mensagens (MTA) é proibido de fazer conversões de texto de mensagem que perdem informações.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9ba4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c9ba4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9ba4-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="c9ba4-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="c9ba4-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9ba4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9ba4-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="c9ba4-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="c9ba4-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9ba4-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9ba4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c9ba4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c9ba4-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9ba4-112">Area:</span></span>  <br/> |<span data-ttu-id="c9ba4-113">Configuração geral</span><span class="sxs-lookup"><span data-stu-id="c9ba4-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9ba4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9ba4-114">Remarks</span></span>

<span data-ttu-id="c9ba4-115">Um exemplo do tipo de conversão que está sendo proibido é o mapeamento "lossy" de Unicode (dois bytes por caractere) para um conjunto de caracteres de um único byte.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c9ba4-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9ba4-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9ba4-117">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c9ba4-117">Header files</span></span>

<span data-ttu-id="c9ba4-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9ba4-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9ba4-119">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9ba4-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9ba4-120">Mapitags.h</span></span>
  
> <span data-ttu-id="c9ba4-121">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9ba4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9ba4-122">See also</span></span>



[<span data-ttu-id="c9ba4-123">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ba4-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9ba4-124">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ba4-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9ba4-125">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9ba4-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9ba4-126">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9ba4-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


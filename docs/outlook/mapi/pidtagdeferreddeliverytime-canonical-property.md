---
title: Propriedade canônica PidTagDeferredDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredDeliveryTime
api_type:
- HeaderDef
ms.assetid: 263ac923-692f-40d4-bdd5-116dc5c49766
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7197159fd55016454de3fa806fc30d0700ef5f3d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359924"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="d11f3-103">Propriedade canônica PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="d11f3-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="d11f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d11f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d11f3-105">Contém a data e a hora em que um remetente de mensagem deseja que uma mensagem seja entregue.</span><span class="sxs-lookup"><span data-stu-id="d11f3-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d11f3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d11f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d11f3-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="d11f3-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="d11f3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d11f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d11f3-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="d11f3-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="d11f3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d11f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="d11f3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d11f3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d11f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d11f3-112">Area:</span></span>  <br/> |<span data-ttu-id="d11f3-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="d11f3-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d11f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d11f3-114">Remarks</span></span>

<span data-ttu-id="d11f3-115">O MAPI não executa a entrega adiada; é uma opção do sistema de mensagens subjacente para lidar com a entrega adiada.</span><span class="sxs-lookup"><span data-stu-id="d11f3-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d11f3-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d11f3-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d11f3-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d11f3-117">Protocol specifications</span></span>

<span data-ttu-id="d11f3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d11f3-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d11f3-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d11f3-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d11f3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d11f3-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d11f3-121">Especifica as propriedades e operações permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="d11f3-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d11f3-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d11f3-122">Header files</span></span>

<span data-ttu-id="d11f3-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d11f3-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d11f3-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d11f3-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d11f3-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d11f3-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d11f3-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d11f3-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d11f3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d11f3-127">See also</span></span>



[<span data-ttu-id="d11f3-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d11f3-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d11f3-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d11f3-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d11f3-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d11f3-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d11f3-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d11f3-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


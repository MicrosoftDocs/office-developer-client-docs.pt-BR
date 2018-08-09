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
ms.openlocfilehash: b6b5f5aa5c595fb0c19ca9b8a9f8aeb94a2c2725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769178"
---
# <a name="pidtagdeferreddeliverytime-canonical-property"></a><span data-ttu-id="484fc-103">Propriedade canônica PidTagDeferredDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="484fc-103">PidTagDeferredDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="484fc-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="484fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="484fc-105">Contém a data e hora quando um remetente da mensagem quiser uma mensagem entregue.</span><span class="sxs-lookup"><span data-stu-id="484fc-105">Contains the date and time when a message sender wants a message delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="484fc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="484fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="484fc-107">PR_DEFERRED_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="484fc-107">PR_DEFERRED_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="484fc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="484fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="484fc-109">0x000F</span><span class="sxs-lookup"><span data-stu-id="484fc-109">0x000F</span></span>  <br/> |
|<span data-ttu-id="484fc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="484fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="484fc-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="484fc-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="484fc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="484fc-112">Area:</span></span>  <br/> |<span data-ttu-id="484fc-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="484fc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="484fc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="484fc-114">Remarks</span></span>

<span data-ttu-id="484fc-115">MAPI não realiza a entrega adiada; é uma opção de sistema de mensagens subjacente para lidar com a entrega adiada.</span><span class="sxs-lookup"><span data-stu-id="484fc-115">MAPI does not perform the deferred delivery; it is an option of the underlying messaging system to handle deferred delivery.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="484fc-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="484fc-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="484fc-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="484fc-117">Protocol specifications</span></span>

<span data-ttu-id="484fc-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="484fc-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="484fc-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="484fc-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="484fc-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="484fc-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="484fc-121">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="484fc-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="484fc-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="484fc-122">Header files</span></span>

<span data-ttu-id="484fc-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="484fc-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="484fc-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="484fc-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="484fc-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="484fc-125">Mapitags.h</span></span>
  
> <span data-ttu-id="484fc-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="484fc-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="484fc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="484fc-127">See also</span></span>



[<span data-ttu-id="484fc-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="484fc-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="484fc-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="484fc-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="484fc-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="484fc-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="484fc-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="484fc-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


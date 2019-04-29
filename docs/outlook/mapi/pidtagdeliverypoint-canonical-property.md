---
title: Propriedade canônica PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439419"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="ad18a-103">Propriedade canônica PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="ad18a-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="ad18a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad18a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad18a-105">Especifica a natureza da entidade funcional por meio da qual uma mensagem foi ou seria entregue ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="ad18a-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad18a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ad18a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ad18a-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="ad18a-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="ad18a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ad18a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ad18a-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="ad18a-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="ad18a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ad18a-110">Data type:</span></span>  <br/> |<span data-ttu-id="ad18a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ad18a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ad18a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ad18a-112">Area:</span></span>  <br/> |<span data-ttu-id="ad18a-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="ad18a-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad18a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad18a-114">Remarks</span></span>

<span data-ttu-id="ad18a-115">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ad18a-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="ad18a-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="ad18a-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="ad18a-117">Entregue a uma lista de distribuição, um ponto de entrega que, por sua vez, pode distribuir a mensagem para muitos destinatários.</span><span class="sxs-lookup"><span data-stu-id="ad18a-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="ad18a-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="ad18a-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="ad18a-119">Entregue a um repositório de mensagens, em vez de diretamente a um destinatário.</span><span class="sxs-lookup"><span data-stu-id="ad18a-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="ad18a-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="ad18a-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="ad18a-121">Entregue a uma unidade de acesso (AU) diferente da PDAU (unidade de acesso de entrega física), como um sistema de FAX.</span><span class="sxs-lookup"><span data-stu-id="ad18a-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="ad18a-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="ad18a-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="ad18a-123">Entregue a uma unidade de acesso físico da entrega, como uma operadora postal humana.</span><span class="sxs-lookup"><span data-stu-id="ad18a-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="ad18a-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="ad18a-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="ad18a-125">Entregue a um sistema de entrega física Patron, como uma caixa postal convencional.</span><span class="sxs-lookup"><span data-stu-id="ad18a-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="ad18a-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="ad18a-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="ad18a-127">Entregue a um agente de usuário privado (UA), como um cliente em um sistema de mensagens interno.</span><span class="sxs-lookup"><span data-stu-id="ad18a-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="ad18a-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="ad18a-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="ad18a-129">Entregue a um agente de usuário público ou um provedor de serviços públicos.</span><span class="sxs-lookup"><span data-stu-id="ad18a-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="ad18a-130">O valor padrão é MAPI_MH_DP_PRIVATE_UA, ou seja, um cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad18a-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ad18a-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad18a-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ad18a-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ad18a-132">Header files</span></span>

<span data-ttu-id="ad18a-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ad18a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="ad18a-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ad18a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="ad18a-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ad18a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="ad18a-136">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ad18a-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ad18a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad18a-137">See also</span></span>



[<span data-ttu-id="ad18a-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ad18a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ad18a-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ad18a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ad18a-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ad18a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ad18a-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ad18a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


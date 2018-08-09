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
ms.openlocfilehash: 803481a71d505fc9f12e77b162a91200cac505d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769179"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="7ec0c-103">Propriedade canônica PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="7ec0c-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="7ec0c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ec0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ec0c-105">Especifica a natureza da entidade funcional por meio do qual uma mensagem foi ou seria foi entregue ao destinatário.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ec0c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7ec0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ec0c-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="7ec0c-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="7ec0c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7ec0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ec0c-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="7ec0c-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="7ec0c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7ec0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ec0c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7ec0c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7ec0c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7ec0c-112">Area:</span></span>  <br/> |<span data-ttu-id="7ec0c-113">Destinatário MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec0c-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ec0c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec0c-114">Remarks</span></span>

<span data-ttu-id="7ec0c-115">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="7ec0c-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="7ec0c-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="7ec0c-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="7ec0c-117">Entregue a uma lista de distribuição, uma ponto de entrega que por sua vez pode distribuir a mensagem para vários destinatários.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="7ec0c-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="7ec0c-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="7ec0c-119">Entregue a um armazenamento de mensagens em vez de diretamente para um destinatário.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="7ec0c-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="7ec0c-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="7ec0c-121">Entregue a uma unidade de acesso (AU) que não seja uma unidade de acesso de entrega física (PDAU), como um sistema de FAX.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="7ec0c-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="7ec0c-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="7ec0c-123">Entregue a uma unidade de acesso de entrega física, como uma operadora de telefonia postal humana.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="7ec0c-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="7ec0c-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="7ec0c-125">Entregue a um sistema de entrega físico patron, como uma caixa de correio postal convencional.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="7ec0c-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="7ec0c-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="7ec0c-127">Entregue a um agente particulares do usuário (UA), como um cliente em um sistema de mensagens na empresa.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="7ec0c-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="7ec0c-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="7ec0c-129">Entregue a um agente de usuário público ou provedor de serviços públicos.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="7ec0c-130">O valor padrão é MAPI_MH_DP_PRIVATE_UA, ou seja, um cliente MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7ec0c-131">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ec0c-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7ec0c-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7ec0c-132">Header files</span></span>

<span data-ttu-id="7ec0c-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ec0c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ec0c-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ec0c-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ec0c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="7ec0c-136">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="7ec0c-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ec0c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec0c-137">See also</span></span>



[<span data-ttu-id="7ec0c-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec0c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ec0c-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7ec0c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ec0c-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec0c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ec0c-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7ec0c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


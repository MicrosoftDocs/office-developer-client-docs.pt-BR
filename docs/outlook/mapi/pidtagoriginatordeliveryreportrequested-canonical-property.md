---
title: Propriedade canônica PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9e508f9c3d84272a0641a27e18c94e0620a7072c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574402"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="0f9dd-103">Propriedade canônica PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="0f9dd-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="0f9dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f9dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f9dd-105">Contém TRUE se o remetente da mensagem solicitar um relatório de entrega para um destinatário específico do sistema de mensagens antes que a mensagem é colocada no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f9dd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0f9dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f9dd-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="0f9dd-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="0f9dd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0f9dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f9dd-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="0f9dd-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="0f9dd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0f9dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f9dd-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0f9dd-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0f9dd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0f9dd-112">Area:</span></span>  <br/> |<span data-ttu-id="0f9dd-113">MIME</span><span class="sxs-lookup"><span data-stu-id="0f9dd-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f9dd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f9dd-114">Remarks</span></span>

<span data-ttu-id="0f9dd-115">Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens entregues.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="0f9dd-116">Nesse caso, a mensagem também forneça primeiro a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="0f9dd-117">A configuração da propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** em uma mensagem é uma maneira de solicitar relatórios de status de entrega para todos os destinatários.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f9dd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f9dd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f9dd-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0f9dd-119">Protocol specifications</span></span>

<span data-ttu-id="0f9dd-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f9dd-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f9dd-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f9dd-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f9dd-122">Header files</span></span>

<span data-ttu-id="0f9dd-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f9dd-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f9dd-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0f9dd-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f9dd-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0f9dd-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0f9dd-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f9dd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f9dd-127">See also</span></span>



[<span data-ttu-id="0f9dd-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0f9dd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f9dd-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0f9dd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f9dd-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0f9dd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f9dd-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0f9dd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


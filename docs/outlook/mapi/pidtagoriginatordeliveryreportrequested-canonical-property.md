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
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395494"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a><span data-ttu-id="6e37f-103">Propriedade canônica PidTagOriginatorDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="6e37f-103">PidTagOriginatorDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="6e37f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e37f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e37f-105">Contém TRUE se o remetente da mensagem solicitar um relatório de entrega para um destinatário específico do sistema de mensagens antes que a mensagem é colocada no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e37f-105">Contains TRUE if a message sender requests a delivery report for a particular recipient from the messaging system before the message is placed in the message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e37f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6e37f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e37f-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="6e37f-107">PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="6e37f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6e37f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e37f-109">0x0023</span><span class="sxs-lookup"><span data-stu-id="6e37f-109">0x0023</span></span>  <br/> |
|<span data-ttu-id="6e37f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6e37f-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e37f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6e37f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6e37f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6e37f-112">Area:</span></span>  <br/> |<span data-ttu-id="6e37f-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6e37f-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e37f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e37f-114">Remarks</span></span>

<span data-ttu-id="6e37f-115">Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens entregues.</span><span class="sxs-lookup"><span data-stu-id="6e37f-115">This property is used to direct the messaging system in handling delivered messages.</span></span> <span data-ttu-id="6e37f-116">Nesse caso, a mensagem também forneça primeiro a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="6e37f-116">In this case, the message must also furnish the **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
<span data-ttu-id="6e37f-117">A configuração da propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** em uma mensagem é uma maneira de solicitar relatórios de status de entrega para todos os destinatários.</span><span class="sxs-lookup"><span data-stu-id="6e37f-117">Setting the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** property on a message is a way to request delivery status reports for all recipients.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e37f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e37f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e37f-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6e37f-119">Protocol specifications</span></span>

<span data-ttu-id="6e37f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e37f-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e37f-121">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6e37f-121">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e37f-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e37f-122">Header files</span></span>

<span data-ttu-id="6e37f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e37f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e37f-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6e37f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e37f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e37f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6e37f-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6e37f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e37f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e37f-127">See also</span></span>



[<span data-ttu-id="6e37f-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6e37f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e37f-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6e37f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e37f-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6e37f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e37f-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6e37f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 86b5d76cab1b85b38d76315cf7d905d1a07f0777
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569061"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="c2353-103">Propriedade canônica PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="c2353-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="c2353-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2353-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2353-105">Contém TRUE se o remetente da mensagem solicitar um relatório de não entrega para um destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="c2353-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2353-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c2353-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2353-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="c2353-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="c2353-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c2353-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2353-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="c2353-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="c2353-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c2353-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2353-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c2353-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c2353-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c2353-112">Area:</span></span>  <br/> |<span data-ttu-id="c2353-113">MIME</span><span class="sxs-lookup"><span data-stu-id="c2353-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2353-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2353-114">Remarks</span></span>

<span data-ttu-id="c2353-115">Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens não entregues.</span><span class="sxs-lookup"><span data-stu-id="c2353-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="c2353-116">Nesse caso, a mensagem também forneça primeiro a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) definida como FALSE.</span><span class="sxs-lookup"><span data-stu-id="c2353-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c2353-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2353-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2353-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c2353-118">Protocol specifications</span></span>

<span data-ttu-id="c2353-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2353-119">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2353-120">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="c2353-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2353-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2353-121">Header files</span></span>

<span data-ttu-id="c2353-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2353-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2353-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c2353-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2353-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2353-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c2353-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c2353-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2353-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2353-126">See also</span></span>



[<span data-ttu-id="c2353-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c2353-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2353-128">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c2353-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2353-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c2353-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2353-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c2353-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


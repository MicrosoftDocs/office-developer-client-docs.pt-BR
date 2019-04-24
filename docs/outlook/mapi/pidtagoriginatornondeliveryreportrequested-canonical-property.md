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
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341955"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a><span data-ttu-id="f5de0-103">Propriedade canônica PidTagOriginatorNonDeliveryReportRequested</span><span class="sxs-lookup"><span data-stu-id="f5de0-103">PidTagOriginatorNonDeliveryReportRequested Canonical Property</span></span>

  
  
<span data-ttu-id="f5de0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5de0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5de0-105">Contém TRUE se um remetente de mensagem solicitar um relatório de não entrega para um destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="f5de0-105">Contains TRUE if a message sender requests a nondelivery report for a particular recipient.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5de0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f5de0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5de0-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="f5de0-107">PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="f5de0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f5de0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5de0-109">0x0C08</span><span class="sxs-lookup"><span data-stu-id="f5de0-109">0x0C08</span></span>  <br/> |
|<span data-ttu-id="f5de0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f5de0-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5de0-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f5de0-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f5de0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f5de0-112">Area:</span></span>  <br/> |<span data-ttu-id="f5de0-113">MIME</span><span class="sxs-lookup"><span data-stu-id="f5de0-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5de0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5de0-114">Remarks</span></span>

<span data-ttu-id="f5de0-115">Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens não entregues.</span><span class="sxs-lookup"><span data-stu-id="f5de0-115">This property is used to direct the messaging system in handling undelivered messages.</span></span> <span data-ttu-id="f5de0-116">Nesse caso, a mensagem também deve fornecer a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) definida como false.</span><span class="sxs-lookup"><span data-stu-id="f5de0-116">In this case, the message must also furnish the **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) property set to FALSE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5de0-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5de0-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5de0-118">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="f5de0-118">Protocol specifications</span></span>

<span data-ttu-id="f5de0-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5de0-119">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5de0-120">Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="f5de0-120">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5de0-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f5de0-121">Header files</span></span>

<span data-ttu-id="f5de0-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f5de0-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5de0-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5de0-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5de0-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f5de0-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f5de0-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f5de0-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5de0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5de0-126">See also</span></span>



[<span data-ttu-id="f5de0-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5de0-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5de0-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f5de0-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5de0-129">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5de0-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5de0-130">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f5de0-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


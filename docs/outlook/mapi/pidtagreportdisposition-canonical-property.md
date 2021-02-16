---
title: Propriedade canônica PidTagReportDisposition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 56b9e7bd-eece-4264-8ee5-a1bcbec4f35c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dae31959cddad7ad61ea32f2372ea34bdbff658e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423703"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="fa069-103">Propriedade canônica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="fa069-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="fa069-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa069-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa069-105">Indica o status do recibo para mensagens que solicitam recibos.</span><span class="sxs-lookup"><span data-stu-id="fa069-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa069-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fa069-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa069-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="fa069-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="fa069-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fa069-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa069-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="fa069-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="fa069-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fa069-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa069-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fa069-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fa069-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fa069-112">Area:</span></span>  <br/> |<span data-ttu-id="fa069-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="fa069-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa069-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa069-114">Remarks</span></span>

<span data-ttu-id="fa069-115">A seguir, os valores válidos:</span><span class="sxs-lookup"><span data-stu-id="fa069-115">The following are valid values:</span></span>
  
- <span data-ttu-id="fa069-116">"deleted"</span><span class="sxs-lookup"><span data-stu-id="fa069-116">"deleted"</span></span>
    
- <span data-ttu-id="fa069-117">"processed"</span><span class="sxs-lookup"><span data-stu-id="fa069-117">"processed"</span></span>
    
- <span data-ttu-id="fa069-118">"dispatched"</span><span class="sxs-lookup"><span data-stu-id="fa069-118">"dispatched"</span></span>
    
- <span data-ttu-id="fa069-119">"denied"</span><span class="sxs-lookup"><span data-stu-id="fa069-119">"denied"</span></span>
    
- <span data-ttu-id="fa069-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="fa069-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="fa069-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa069-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa069-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fa069-122">Protocol specifications</span></span>

<span data-ttu-id="fa069-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="fa069-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="fa069-124">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fa069-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa069-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="fa069-125">Header files</span></span>

<span data-ttu-id="fa069-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa069-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa069-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fa069-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa069-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fa069-128">Mapitags.h</span></span>
  
> <span data-ttu-id="fa069-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="fa069-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa069-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa069-130">See also</span></span>



[<span data-ttu-id="fa069-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fa069-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa069-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fa069-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa069-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fa069-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa069-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fa069-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


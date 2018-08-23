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
ms.openlocfilehash: 1e84308f3a9f9457c5db23c1ad9d42d6e856519e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583628"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="408bd-103">Propriedade canônica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="408bd-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="408bd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="408bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="408bd-105">Indica o status de recebimento de mensagens com solicitar confirmações.</span><span class="sxs-lookup"><span data-stu-id="408bd-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="408bd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="408bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="408bd-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="408bd-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="408bd-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="408bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="408bd-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="408bd-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="408bd-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="408bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="408bd-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="408bd-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="408bd-112">Área:</span><span class="sxs-lookup"><span data-stu-id="408bd-112">Area:</span></span>  <br/> |<span data-ttu-id="408bd-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="408bd-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="408bd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="408bd-114">Remarks</span></span>

<span data-ttu-id="408bd-115">Estes são valores válidos:</span><span class="sxs-lookup"><span data-stu-id="408bd-115">The following are valid values:</span></span>
  
- <span data-ttu-id="408bd-116">"excluída"</span><span class="sxs-lookup"><span data-stu-id="408bd-116">"deleted"</span></span>
    
- <span data-ttu-id="408bd-117">"processadas"</span><span class="sxs-lookup"><span data-stu-id="408bd-117">"processed"</span></span>
    
- <span data-ttu-id="408bd-118">"despachado"</span><span class="sxs-lookup"><span data-stu-id="408bd-118">"dispatched"</span></span>
    
- <span data-ttu-id="408bd-119">"negado"</span><span class="sxs-lookup"><span data-stu-id="408bd-119">"denied"</span></span>
    
- <span data-ttu-id="408bd-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="408bd-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="408bd-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="408bd-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="408bd-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="408bd-122">Protocol specifications</span></span>

<span data-ttu-id="408bd-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="408bd-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="408bd-124">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="408bd-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="408bd-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="408bd-125">Header files</span></span>

<span data-ttu-id="408bd-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="408bd-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="408bd-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="408bd-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="408bd-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="408bd-128">Mapitags.h</span></span>
  
> <span data-ttu-id="408bd-129">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="408bd-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="408bd-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="408bd-130">See also</span></span>



[<span data-ttu-id="408bd-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="408bd-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="408bd-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="408bd-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="408bd-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="408bd-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="408bd-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="408bd-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


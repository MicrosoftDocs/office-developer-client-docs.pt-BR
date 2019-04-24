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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346351"
---
# <a name="pidtagreportdisposition-canonical-property"></a><span data-ttu-id="3e1cc-103">Propriedade canônica PidTagReportDisposition</span><span class="sxs-lookup"><span data-stu-id="3e1cc-103">PidTagReportDisposition Canonical Property</span></span>

  
  
<span data-ttu-id="3e1cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e1cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e1cc-105">Indica o status de recebimento das mensagens que solicitam recebimentos.</span><span class="sxs-lookup"><span data-stu-id="3e1cc-105">Indicates the receipt status for messages that request receipts.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3e1cc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3e1cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3e1cc-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span><span class="sxs-lookup"><span data-stu-id="3e1cc-107">PR_REPORT_DISPOSITION, PR_REPORT_DISPOSITION_A, PR_REPORT_DISPOSITION_W</span></span>  <br/> |
|<span data-ttu-id="3e1cc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3e1cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3e1cc-109">0x0080</span><span class="sxs-lookup"><span data-stu-id="3e1cc-109">0x0080</span></span>  <br/> |
|<span data-ttu-id="3e1cc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3e1cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="3e1cc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3e1cc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3e1cc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3e1cc-112">Area:</span></span>  <br/> |<span data-ttu-id="3e1cc-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="3e1cc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e1cc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e1cc-114">Remarks</span></span>

<span data-ttu-id="3e1cc-115">A seguir estão valores válidos:</span><span class="sxs-lookup"><span data-stu-id="3e1cc-115">The following are valid values:</span></span>
  
- <span data-ttu-id="3e1cc-116">excluídos</span><span class="sxs-lookup"><span data-stu-id="3e1cc-116">"deleted"</span></span>
    
- <span data-ttu-id="3e1cc-117">processa</span><span class="sxs-lookup"><span data-stu-id="3e1cc-117">"processed"</span></span>
    
- <span data-ttu-id="3e1cc-118">expedidos</span><span class="sxs-lookup"><span data-stu-id="3e1cc-118">"dispatched"</span></span>
    
- <span data-ttu-id="3e1cc-119">recusa</span><span class="sxs-lookup"><span data-stu-id="3e1cc-119">"denied"</span></span>
    
- <span data-ttu-id="3e1cc-120">"failed"</span><span class="sxs-lookup"><span data-stu-id="3e1cc-120">"failed"</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3e1cc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e1cc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3e1cc-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3e1cc-122">Protocol specifications</span></span>

<span data-ttu-id="3e1cc-123">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3e1cc-123">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3e1cc-124">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3e1cc-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3e1cc-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3e1cc-125">Header files</span></span>

<span data-ttu-id="3e1cc-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3e1cc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="3e1cc-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3e1cc-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="3e1cc-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3e1cc-128">Mapitags.h</span></span>
  
> <span data-ttu-id="3e1cc-129">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3e1cc-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3e1cc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e1cc-130">See also</span></span>



[<span data-ttu-id="3e1cc-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3e1cc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3e1cc-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3e1cc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3e1cc-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3e1cc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3e1cc-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3e1cc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


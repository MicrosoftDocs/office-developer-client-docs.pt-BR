---
title: Propriedade canônica PidTagReportTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c832842568ea3d64d50b56d226b66d551402ba6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769844"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="6e0db-103">Propriedade canônica PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="6e0db-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="6e0db-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e0db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e0db-105">Contém um valor binário marca que o sistema de mensagens deve copiar a qualquer relatório gerado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6e0db-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e0db-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6e0db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e0db-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="6e0db-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="6e0db-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6e0db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e0db-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="6e0db-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="6e0db-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6e0db-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e0db-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6e0db-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6e0db-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6e0db-112">Area:</span></span>  <br/> |<span data-ttu-id="6e0db-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="6e0db-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e0db-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e0db-114">Remarks</span></span>

<span data-ttu-id="6e0db-115">Essa propriedade, como a propriedade **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)), é usada para correlacionar um relatório com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="6e0db-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6e0db-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e0db-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6e0db-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6e0db-117">Protocol specifications</span></span>

<span data-ttu-id="6e0db-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e0db-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e0db-119">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6e0db-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6e0db-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6e0db-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6e0db-121">Especifica as propriedades e operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="6e0db-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6e0db-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e0db-122">Header files</span></span>

<span data-ttu-id="6e0db-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e0db-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e0db-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6e0db-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e0db-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6e0db-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6e0db-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6e0db-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e0db-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e0db-127">See also</span></span>



[<span data-ttu-id="6e0db-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6e0db-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e0db-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6e0db-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e0db-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6e0db-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e0db-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6e0db-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331427"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="81617-103">Propriedade canônica PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="81617-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="81617-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81617-105">Contém um valor de marca binária que o sistema de mensagens deve copiar para qualquer relatório gerado para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="81617-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81617-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="81617-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81617-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="81617-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="81617-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81617-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81617-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="81617-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="81617-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="81617-110">Data type:</span></span>  <br/> |<span data-ttu-id="81617-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="81617-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="81617-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81617-112">Area:</span></span>  <br/> |<span data-ttu-id="81617-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="81617-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81617-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81617-114">Remarks</span></span>

<span data-ttu-id="81617-115">Essa propriedade, como a propriedade **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)), é usada para correlacionar um relatório com a mensagem original.</span><span class="sxs-lookup"><span data-stu-id="81617-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81617-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81617-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81617-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="81617-117">Protocol specifications</span></span>

<span data-ttu-id="81617-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81617-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81617-119">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="81617-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81617-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81617-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81617-121">Especifica as propriedades e as operações que são permitidas em mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="81617-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81617-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81617-122">Header files</span></span>

<span data-ttu-id="81617-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="81617-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="81617-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="81617-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="81617-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="81617-125">Mapitags.h</span></span>
  
> <span data-ttu-id="81617-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="81617-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81617-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="81617-127">See also</span></span>



[<span data-ttu-id="81617-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81617-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81617-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="81617-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81617-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="81617-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81617-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="81617-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


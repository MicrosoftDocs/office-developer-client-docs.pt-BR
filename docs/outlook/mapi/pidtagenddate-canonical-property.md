---
title: Propriedade canônica PidTagEndDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361058"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="d0456-103">Propriedade canônica PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="d0456-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="d0456-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0456-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0456-105">Contém a data e a hora de término de um compromisso como gerenciados por um aplicativo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="d0456-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0456-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d0456-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0456-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="d0456-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="d0456-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0456-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0456-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="d0456-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="d0456-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d0456-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0456-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d0456-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d0456-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d0456-112">Area:</span></span>  <br/> |<span data-ttu-id="d0456-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="d0456-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0456-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0456-114">Remarks</span></span>

<span data-ttu-id="d0456-115">Os aplicativos de agendamento devem definir a **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) e essa propriedade ao enviar solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="d0456-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0456-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0456-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d0456-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d0456-117">Protocol specifications</span></span>

<span data-ttu-id="d0456-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0456-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0456-119">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d0456-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0456-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0456-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0456-121">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="d0456-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0456-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d0456-122">Header files</span></span>

<span data-ttu-id="d0456-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0456-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0456-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d0456-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0456-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0456-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d0456-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d0456-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0456-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0456-127">See also</span></span>



[<span data-ttu-id="d0456-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d0456-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0456-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d0456-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0456-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d0456-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0456-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d0456-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


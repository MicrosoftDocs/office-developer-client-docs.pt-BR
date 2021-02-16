---
title: Propriedade canônica PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5ead258c056ec2204ddab92e9b99e1b17fe98092
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330083"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="7d064-103">Propriedade canônica PidTagScheduleInfoDisallowOverlappingAppts</span><span class="sxs-lookup"><span data-stu-id="7d064-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="7d064-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d064-105">Contém TRUE se compromissos sobrepostos não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="7d064-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d064-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7d064-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d064-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="7d064-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="7d064-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d064-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d064-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="7d064-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="7d064-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7d064-110">Data type:</span></span>  <br/> |<span data-ttu-id="7d064-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="7d064-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="7d064-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d064-112">Area:</span></span>  <br/> |<span data-ttu-id="7d064-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="7d064-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d064-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d064-114">Remarks</span></span>

<span data-ttu-id="7d064-115">Essa propriedade só será significativa quando o valor da propriedade **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) for VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="7d064-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="7d064-116">Um valor TRUE indica que, ao responder automaticamente a solicitações de reunião, um cliente ou servidor deve recusar instâncias que se sobreponham a eventos agendados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7d064-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="7d064-117">Um valor FALSE ou a ausência dessa propriedade indica que instâncias sobrepostas devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="7d064-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="7d064-118">Esta não é uma propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="7d064-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7d064-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d064-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d064-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d064-120">Protocol specifications</span></span>

<span data-ttu-id="7d064-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d064-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d064-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7d064-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7d064-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d064-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d064-124">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="7d064-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="7d064-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d064-125">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d064-126">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="7d064-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d064-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7d064-127">Header files</span></span>

<span data-ttu-id="7d064-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d064-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d064-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7d064-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d064-130">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d064-130">Mapitags.h</span></span>
  
> <span data-ttu-id="7d064-131">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7d064-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d064-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d064-132">See also</span></span>



[<span data-ttu-id="7d064-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d064-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d064-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7d064-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d064-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d064-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d064-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7d064-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


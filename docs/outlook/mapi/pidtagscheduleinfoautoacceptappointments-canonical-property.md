---
title: Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386884"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="8c45c-103">Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="8c45c-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="8c45c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c45c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c45c-105">Conterá TRUE se um cliente ou servidor automaticamente deve responder a todas as solicitações de reunião para o recurso ou participante.</span><span class="sxs-lookup"><span data-stu-id="8c45c-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c45c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8c45c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c45c-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="8c45c-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="8c45c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8c45c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c45c-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="8c45c-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="8c45c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8c45c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c45c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8c45c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8c45c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8c45c-112">Area:</span></span>  <br/> |<span data-ttu-id="8c45c-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="8c45c-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c45c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c45c-114">Remarks</span></span>

<span data-ttu-id="8c45c-115">Ao responder, a resposta deve ser aceitação, a menos que uma restrição adicional que é especificado pela **PR_SCHDINFO_DISALLOW_ ou **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) OVERLAPPING_APPTS** propriedades ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) for atingido.</span><span class="sxs-lookup"><span data-stu-id="8c45c-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="8c45c-116">Um valor falso ou a ausência dessa propriedade indica que um cliente ou servidor deve não aceitar automaticamente solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="8c45c-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="8c45c-117">Isso não é uma propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="8c45c-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8c45c-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c45c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c45c-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8c45c-119">Protocol specifications</span></span>

<span data-ttu-id="8c45c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c45c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c45c-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8c45c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c45c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c45c-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c45c-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="8c45c-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8c45c-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c45c-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c45c-125">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="8c45c-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c45c-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c45c-126">Header files</span></span>

<span data-ttu-id="8c45c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c45c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c45c-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c45c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c45c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c45c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8c45c-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c45c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c45c-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c45c-131">See also</span></span>



[<span data-ttu-id="8c45c-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c45c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c45c-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8c45c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c45c-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8c45c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c45c-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8c45c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330090"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="0a06f-103">Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="0a06f-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="0a06f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a06f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a06f-105">Contém TRUE se um cliente ou servidor deve responder automaticamente a todas as solicitações de reunião do participante ou recurso.</span><span class="sxs-lookup"><span data-stu-id="0a06f-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a06f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0a06f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a06f-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="0a06f-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="0a06f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0a06f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a06f-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="0a06f-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="0a06f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0a06f-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a06f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0a06f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0a06f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0a06f-112">Area:</span></span>  <br/> |<span data-ttu-id="0a06f-113">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="0a06f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a06f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a06f-114">Remarks</span></span>

<span data-ttu-id="0a06f-115">Ao responder, a resposta deve ser aceita, a menos que uma restrição adicional especificada pelo **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) Propriedades é atendida.</span><span class="sxs-lookup"><span data-stu-id="0a06f-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="0a06f-116">Um valor FALSE ou a ausência dessa propriedade indica que um cliente ou servidor não deve aceitar automaticamente solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="0a06f-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="0a06f-117">Essa não é uma propriedade obrigatória.</span><span class="sxs-lookup"><span data-stu-id="0a06f-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a06f-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a06f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a06f-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="0a06f-119">Protocol specifications</span></span>

<span data-ttu-id="0a06f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a06f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a06f-121">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0a06f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a06f-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a06f-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a06f-123">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="0a06f-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0a06f-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a06f-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a06f-125">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="0a06f-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a06f-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0a06f-126">Header files</span></span>

<span data-ttu-id="0a06f-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0a06f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a06f-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0a06f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a06f-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0a06f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0a06f-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0a06f-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a06f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a06f-131">See also</span></span>



[<span data-ttu-id="0a06f-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0a06f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a06f-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0a06f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a06f-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0a06f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a06f-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0a06f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


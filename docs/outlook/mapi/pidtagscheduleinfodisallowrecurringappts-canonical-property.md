---
title: Propriedade canônica PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f5f3feb5b3186f8d0239558aa410c7f71bdf54f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769953"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="029ca-103">Propriedade canônica PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="029ca-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="029ca-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="029ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="029ca-105">Contém TRUE quando a resposta automática para compromissos recorrentes recusar.</span><span class="sxs-lookup"><span data-stu-id="029ca-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="029ca-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="029ca-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="029ca-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="029ca-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="029ca-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="029ca-108">Identifier:</span></span>  <br/> |<span data-ttu-id="029ca-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="029ca-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="029ca-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="029ca-110">Data type:</span></span>  <br/> |<span data-ttu-id="029ca-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="029ca-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="029ca-112">Área:</span><span class="sxs-lookup"><span data-stu-id="029ca-112">Area:</span></span>  <br/> |<span data-ttu-id="029ca-113">Informações de disponibilidade</span><span class="sxs-lookup"><span data-stu-id="029ca-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="029ca-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="029ca-114">Remarks</span></span>

<span data-ttu-id="029ca-115">Essa propriedade é significativa apenas quando o valor da propriedade **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) é TRUE.</span><span class="sxs-lookup"><span data-stu-id="029ca-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="029ca-116">A ausência dessa propriedade indica que as reuniões recorrentes devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="029ca-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="029ca-117">Isso não é uma propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="029ca-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="029ca-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="029ca-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="029ca-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="029ca-119">Protocol specifications</span></span>

<span data-ttu-id="029ca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ca-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ca-121">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="029ca-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="029ca-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ca-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ca-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="029ca-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="029ca-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="029ca-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="029ca-125">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="029ca-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="029ca-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="029ca-126">Header files</span></span>

<span data-ttu-id="029ca-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="029ca-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="029ca-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="029ca-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="029ca-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="029ca-129">Mapitags.h</span></span>
  
> <span data-ttu-id="029ca-130">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="029ca-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="029ca-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="029ca-131">See also</span></span>



[<span data-ttu-id="029ca-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="029ca-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="029ca-133">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="029ca-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="029ca-134">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="029ca-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="029ca-135">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="029ca-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

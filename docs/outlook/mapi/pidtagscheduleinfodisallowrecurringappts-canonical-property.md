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
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330097"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="008e8-103">Propriedade canônica PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="008e8-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="008e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="008e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="008e8-105">Contém VERDADEIRO quando a resposta automática a compromissos recorrentes é recusada.</span><span class="sxs-lookup"><span data-stu-id="008e8-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="008e8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="008e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="008e8-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="008e8-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="008e8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="008e8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="008e8-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="008e8-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="008e8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="008e8-110">Data type:</span></span>  <br/> |<span data-ttu-id="008e8-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="008e8-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="008e8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="008e8-112">Area:</span></span>  <br/> |<span data-ttu-id="008e8-113">Livre/Ocupado</span><span class="sxs-lookup"><span data-stu-id="008e8-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="008e8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="008e8-114">Remarks</span></span>

<span data-ttu-id="008e8-115">Essa propriedade só será significativa quando o valor da propriedade **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) for VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="008e8-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="008e8-116">A ausência dessa propriedade indica que reuniões recorrentes devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="008e8-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="008e8-117">Esta não é uma propriedade necessária.</span><span class="sxs-lookup"><span data-stu-id="008e8-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="008e8-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="008e8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="008e8-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="008e8-119">Protocol specifications</span></span>

<span data-ttu-id="008e8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="008e8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="008e8-121">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="008e8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="008e8-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="008e8-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="008e8-123">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="008e8-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="008e8-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="008e8-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="008e8-125">Publica a disponibilidade de um usuário ou recurso.</span><span class="sxs-lookup"><span data-stu-id="008e8-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="008e8-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="008e8-126">Header files</span></span>

<span data-ttu-id="008e8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="008e8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="008e8-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="008e8-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="008e8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="008e8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="008e8-130">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="008e8-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="008e8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="008e8-131">See also</span></span>



[<span data-ttu-id="008e8-132">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="008e8-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="008e8-133">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="008e8-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="008e8-134">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="008e8-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="008e8-135">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="008e8-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


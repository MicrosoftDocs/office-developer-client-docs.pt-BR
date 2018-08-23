---
title: Propriedade canônica PidLidRecurrencePattern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurrencePattern
api_type:
- COM
ms.assetid: ac21ba98-f16b-4365-9134-bca7748189ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 12a55ec4dfe0fb53a07aef73cb4e96771379e483
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589221"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="75d14-103">Propriedade canônica PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="75d14-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="75d14-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75d14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75d14-105">Especifica uma descrição do padrão de recorrência do objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="75d14-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="75d14-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="75d14-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75d14-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="75d14-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="75d14-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="75d14-108">Property set:</span></span>  <br/> |<span data-ttu-id="75d14-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="75d14-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="75d14-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="75d14-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="75d14-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="75d14-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="75d14-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="75d14-112">Data type:</span></span>  <br/> |<span data-ttu-id="75d14-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="75d14-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="75d14-114">Área:</span><span class="sxs-lookup"><span data-stu-id="75d14-114">Area:</span></span>  <br/> |<span data-ttu-id="75d14-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="75d14-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75d14-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="75d14-116">Remarks</span></span>

<span data-ttu-id="75d14-117">Se essa propriedade estiver definida, ela deve ser definida como uma descrição da recorrência que é especificada pela propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="75d14-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="75d14-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75d14-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75d14-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="75d14-119">Protocol specifications</span></span>

<span data-ttu-id="75d14-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75d14-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75d14-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="75d14-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75d14-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75d14-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75d14-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="75d14-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75d14-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75d14-124">Header files</span></span>

<span data-ttu-id="75d14-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75d14-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="75d14-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75d14-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75d14-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="75d14-127">See also</span></span>



[<span data-ttu-id="75d14-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75d14-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75d14-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="75d14-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75d14-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="75d14-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75d14-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="75d14-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


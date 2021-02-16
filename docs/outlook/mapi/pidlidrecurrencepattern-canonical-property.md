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
ms.openlocfilehash: d94ac430df54fc03d96ac761c53ca20201d899c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315929"
---
# <a name="pidlidrecurrencepattern-canonical-property"></a><span data-ttu-id="10151-103">Propriedade canônica PidLidRecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="10151-103">PidLidRecurrencePattern Canonical Property</span></span>

  
  
<span data-ttu-id="10151-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10151-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10151-105">Especifica uma descrição do padrão de recorrência do objeto de calendário.</span><span class="sxs-lookup"><span data-stu-id="10151-105">Specifies a description of the recurrence pattern of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10151-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="10151-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10151-107">dispidRecurPattern</span><span class="sxs-lookup"><span data-stu-id="10151-107">dispidRecurPattern</span></span>  <br/> |
|<span data-ttu-id="10151-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="10151-108">Property set:</span></span>  <br/> |<span data-ttu-id="10151-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="10151-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="10151-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="10151-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10151-111">0x00008232</span><span class="sxs-lookup"><span data-stu-id="10151-111">0x00008232</span></span>  <br/> |
|<span data-ttu-id="10151-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="10151-112">Data type:</span></span>  <br/> |<span data-ttu-id="10151-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="10151-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="10151-114">Área:</span><span class="sxs-lookup"><span data-stu-id="10151-114">Area:</span></span>  <br/> |<span data-ttu-id="10151-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="10151-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10151-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10151-116">Remarks</span></span>

<span data-ttu-id="10151-117">Se essa propriedade for definida, ela deverá ser definida como uma descrição da recorrência especificada pela **propriedade dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10151-117">If this property is set, it must be set to a description of the recurrence that is specified by the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10151-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="10151-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10151-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="10151-119">Protocol specifications</span></span>

<span data-ttu-id="10151-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10151-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10151-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="10151-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10151-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10151-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10151-123">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="10151-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10151-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="10151-124">Header files</span></span>

<span data-ttu-id="10151-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10151-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10151-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="10151-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10151-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="10151-127">See also</span></span>



[<span data-ttu-id="10151-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="10151-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10151-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="10151-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10151-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="10151-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10151-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="10151-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


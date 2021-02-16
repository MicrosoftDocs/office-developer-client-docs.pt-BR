---
title: Propriedade canônica PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: eaff90de919c1bdc04983bce32a2aa808ae56013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358895"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="9b33b-103">Propriedade canônica PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="9b33b-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="9b33b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b33b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b33b-105">Representa a data e a hora em que um compromisso termina.</span><span class="sxs-lookup"><span data-stu-id="9b33b-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9b33b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="9b33b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9b33b-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="9b33b-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="9b33b-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="9b33b-108">Property set:</span></span>  <br/> |<span data-ttu-id="9b33b-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="9b33b-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="9b33b-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="9b33b-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9b33b-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="9b33b-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="9b33b-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="9b33b-112">Data type:</span></span>  <br/> |<span data-ttu-id="9b33b-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="9b33b-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="9b33b-114">Área:</span><span class="sxs-lookup"><span data-stu-id="9b33b-114">Area:</span></span>  <br/> |<span data-ttu-id="9b33b-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="9b33b-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b33b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b33b-116">Remarks</span></span>

<span data-ttu-id="9b33b-117">Essa propriedade corresponde à propriedade **dispidApptEndWhole** do compromisso no modelo de objeto do Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b33b-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="9b33b-118">Isso especifica a data e a hora de término do evento; ele deve estar no Tempo Universal Coordenado (UTC) e deve ser maior do que o valor da propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="9b33b-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="9b33b-119">Para uma série recorrente, a **propriedade dispidApptEndWhole** é a data e hora de término da primeira instância de acordo com o padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="9b33b-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9b33b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b33b-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9b33b-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="9b33b-121">Protocol specifications</span></span>

<span data-ttu-id="9b33b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b33b-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b33b-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9b33b-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9b33b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9b33b-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9b33b-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="9b33b-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9b33b-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="9b33b-126">Header files</span></span>

<span data-ttu-id="9b33b-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b33b-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9b33b-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="9b33b-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b33b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b33b-129">See also</span></span>



[<span data-ttu-id="9b33b-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="9b33b-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9b33b-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="9b33b-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9b33b-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="9b33b-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9b33b-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="9b33b-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.openlocfilehash: 21d1ee071aa5df24d0ddf641ff6f458a7de1cb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594275"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a><span data-ttu-id="5b11a-103">Propriedade canônica PidLidAppointmentEndWhole</span><span class="sxs-lookup"><span data-stu-id="5b11a-103">PidLidAppointmentEndWhole Canonical Property</span></span>

  
  
<span data-ttu-id="5b11a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b11a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b11a-105">Representa a data e hora de término de um compromisso.</span><span class="sxs-lookup"><span data-stu-id="5b11a-105">Represents the date and time that an appointment ends.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b11a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5b11a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b11a-107">dispidApptEndWhole</span><span class="sxs-lookup"><span data-stu-id="5b11a-107">dispidApptEndWhole</span></span>  <br/> |
|<span data-ttu-id="5b11a-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5b11a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5b11a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5b11a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5b11a-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5b11a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5b11a-111">0x0000820E</span><span class="sxs-lookup"><span data-stu-id="5b11a-111">0x0000820E</span></span>  <br/> |
|<span data-ttu-id="5b11a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5b11a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5b11a-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5b11a-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5b11a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5b11a-114">Area:</span></span>  <br/> |<span data-ttu-id="5b11a-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="5b11a-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b11a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b11a-116">Remarks</span></span>

<span data-ttu-id="5b11a-117">Essa propriedade corresponde à propriedade **dispidApptEndWhole** do compromisso no modelo de objeto do Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="5b11a-117">This property corresponds to the **dispidApptEndWhole** property of the appointment in the Microsoft Office Outlook object model.</span></span> 
  
<span data-ttu-id="5b11a-118">Especifica a data de término e a hora do evento; ela deve ser no tempo Universal Coordenado (UTC) e deve ser maior que o valor da propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5b11a-118">This specifies the end date and time for the event; it must be in Coordinated Universal Time (UTC) and must be greater than the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="5b11a-119">Para uma série recorrente, a propriedade **dispidApptEndWhole** é a data de término e a hora da instância do primeira de acordo com o padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="5b11a-119">For a recurring series, the **dispidApptEndWhole** property is the end date and time of the first instance according to the recurrence pattern.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5b11a-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b11a-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5b11a-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5b11a-121">Protocol specifications</span></span>

<span data-ttu-id="5b11a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b11a-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b11a-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b11a-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5b11a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5b11a-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5b11a-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5b11a-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5b11a-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5b11a-126">Header files</span></span>

<span data-ttu-id="5b11a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5b11a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b11a-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5b11a-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b11a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b11a-129">See also</span></span>



[<span data-ttu-id="5b11a-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b11a-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b11a-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5b11a-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b11a-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5b11a-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b11a-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5b11a-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


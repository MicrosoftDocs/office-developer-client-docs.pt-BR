---
title: Propriedade canônica PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345413"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="b35fc-103">Propriedade canônica PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="b35fc-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="b35fc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b35fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b35fc-105">Especifica se o evento é ou não o dia inteiro.</span><span class="sxs-lookup"><span data-stu-id="b35fc-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b35fc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b35fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b35fc-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="b35fc-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="b35fc-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b35fc-108">Property set:</span></span>  <br/> |<span data-ttu-id="b35fc-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b35fc-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b35fc-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b35fc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b35fc-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="b35fc-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="b35fc-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b35fc-112">Data type:</span></span>  <br/> |<span data-ttu-id="b35fc-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b35fc-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b35fc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b35fc-114">Area:</span></span>  <br/> |<span data-ttu-id="b35fc-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="b35fc-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b35fc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b35fc-116">Remarks</span></span>

<span data-ttu-id="b35fc-117">Essa propriedade especifica se o evento é ou não um evento de dia inteiro, conforme especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b35fc-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="b35fc-118">Um valor TRUE indica que o evento é um evento de dia inteiro; nesse caso, a hora de início e a hora de término devem ser meia-noite, de modo que a duração seja múltipla de 24 horas e seja pelo menos 24 horas.</span><span class="sxs-lookup"><span data-stu-id="b35fc-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="b35fc-119">Um valor FALSE ou a ausência dessa propriedade indica que o evento não é um evento de dia inteiro.</span><span class="sxs-lookup"><span data-stu-id="b35fc-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="b35fc-120">O cliente ou servidor não deve inferir o valor como TRUE quando um usuário cria um evento de 24 horas, mesmo se o evento começa e termina à meia-noite.</span><span class="sxs-lookup"><span data-stu-id="b35fc-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b35fc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b35fc-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b35fc-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b35fc-122">Protocol specifications</span></span>

<span data-ttu-id="b35fc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b35fc-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b35fc-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b35fc-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b35fc-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b35fc-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b35fc-126">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="b35fc-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b35fc-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b35fc-127">Header files</span></span>

<span data-ttu-id="b35fc-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b35fc-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b35fc-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b35fc-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b35fc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b35fc-130">See also</span></span>



[<span data-ttu-id="b35fc-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b35fc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b35fc-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b35fc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b35fc-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b35fc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b35fc-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b35fc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


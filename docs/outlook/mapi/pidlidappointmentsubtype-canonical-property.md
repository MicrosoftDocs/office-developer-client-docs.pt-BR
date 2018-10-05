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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385876"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a><span data-ttu-id="82446-103">Propriedade canônica PidLidAppointmentSubType</span><span class="sxs-lookup"><span data-stu-id="82446-103">PidLidAppointmentSubType Canonical Property</span></span>

  
  
<span data-ttu-id="82446-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82446-105">Especifica se é ou não o evento durante todo o dia.</span><span class="sxs-lookup"><span data-stu-id="82446-105">Specifies whether or not the event is all day.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="82446-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="82446-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82446-107">dispidApptSubType</span><span class="sxs-lookup"><span data-stu-id="82446-107">dispidApptSubType</span></span>  <br/> |
|<span data-ttu-id="82446-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="82446-108">Property set:</span></span>  <br/> |<span data-ttu-id="82446-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="82446-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="82446-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="82446-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="82446-111">0x00008215</span><span class="sxs-lookup"><span data-stu-id="82446-111">0x00008215</span></span>  <br/> |
|<span data-ttu-id="82446-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="82446-112">Data type:</span></span>  <br/> |<span data-ttu-id="82446-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="82446-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="82446-114">Área:</span><span class="sxs-lookup"><span data-stu-id="82446-114">Area:</span></span>  <br/> |<span data-ttu-id="82446-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="82446-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82446-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="82446-116">Remarks</span></span>

<span data-ttu-id="82446-117">Esta propriedade especifica se é ou não o evento um evento de dia inteiro, conforme especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="82446-117">This property specifies whether or not the event is an all-day event, as specified by the user.</span></span> <span data-ttu-id="82446-118">Um valor TRUE indica que o evento é um evento de dia inteiro, caso em que a hora de início e hora de término devem ser meia-noite para que a duração é um múltiplo de 24 horas e é pelo menos 24 horas.</span><span class="sxs-lookup"><span data-stu-id="82446-118">A value of TRUE indicates that the event is an all-day event, in which case the start time and end time must be midnight so that the duration is a multiple of 24 hours and is at least 24 hours.</span></span> <span data-ttu-id="82446-119">Um valor falso ou a ausência dessa propriedade indica que o evento não é um evento de dia inteiro.</span><span class="sxs-lookup"><span data-stu-id="82446-119">A value of FALSE or the absence of this property indicates the event is not an all-day event.</span></span> <span data-ttu-id="82446-120">O cliente ou servidor não deve interpretar o valor como TRUE quando um usuário acontece criar um evento que é de 24 horas, mesmo se o evento inicia e termina à meia-noite.</span><span class="sxs-lookup"><span data-stu-id="82446-120">The client or server must not infer the value as TRUE when a user happens to create an event that is 24 hours, even if the event starts and ends at midnight.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82446-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="82446-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82446-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="82446-122">Protocol specifications</span></span>

<span data-ttu-id="82446-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82446-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82446-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="82446-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82446-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82446-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82446-126">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="82446-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82446-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82446-127">Header files</span></span>

<span data-ttu-id="82446-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="82446-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="82446-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="82446-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82446-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="82446-130">See also</span></span>



[<span data-ttu-id="82446-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="82446-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82446-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="82446-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82446-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="82446-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82446-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="82446-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionEndDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionEndDisplay
api_type:
- COM
ms.assetid: 7b6193cb-612b-408e-b9bc-285df313e2cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 24ccd25a1d799f3146bd230e5156be0051104f47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345378"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="296d2-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="296d2-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="296d2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="296d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="296d2-105">Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que armazena a descrição para o fuso horário que é usado quando a hora de término de um compromisso de instância única ou solicitação de reunião é selecionada.</span><span class="sxs-lookup"><span data-stu-id="296d2-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="296d2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="296d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="296d2-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="296d2-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="296d2-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="296d2-108">Property set:</span></span>  <br/> |<span data-ttu-id="296d2-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="296d2-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="296d2-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="296d2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="296d2-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="296d2-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="296d2-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="296d2-112">Data type:</span></span>  <br/> |<span data-ttu-id="296d2-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="296d2-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="296d2-114">Área:</span><span class="sxs-lookup"><span data-stu-id="296d2-114">Area:</span></span>  <br/> |<span data-ttu-id="296d2-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="296d2-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="296d2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="296d2-116">Remarks</span></span>

<span data-ttu-id="296d2-117">Microsoft Office Outlook 2003 ou anterior, e soluções baseadas no CDO (Collaboration Data Objects) 1.2.1 e que não executaram a ferramenta de atualização de calendário para o Outlook ou o Microsoft Exchange Server, armazene a hora de início e a hora de término de compromissos de instância única e solicitações de reunião em UTC (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="296d2-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="296d2-118">Esses clientes não armazenam informações para o fuso horário em que a solicitação de compromisso ou reunião é criada.</span><span class="sxs-lookup"><span data-stu-id="296d2-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="296d2-119">As versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e as soluções baseadas no CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam **dispidApptTZDefEndDisplay** para armazenar o fuso horário para a hora de término.</span><span class="sxs-lookup"><span data-stu-id="296d2-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="296d2-120">**dispidApptTZDefEndDisplay** mostra o compromisso ou a reunião no fuso horário original que foi agendado e determina se a hora de término deve ser ajustada se as regras do fuso horário mudarem.</span><span class="sxs-lookup"><span data-stu-id="296d2-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="296d2-121">Se essa propriedade estiver ausente, o fuso horário especificado pela **propriedade dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) será usado.</span><span class="sxs-lookup"><span data-stu-id="296d2-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="296d2-122">Se **dispidApptTZDefStartDisplay** estiver ausente ou for inválido, o fuso horário local atual será considerado.</span><span class="sxs-lookup"><span data-stu-id="296d2-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="296d2-123">**dispidApptTZDefEndDisplay** é usado apenas para fins de exibição e não é usado na expansão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="296d2-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="296d2-124">Um analisador deve ter cuidado ao ler um fluxo obtido de **dispidApptTZDefEndDisplay** ou quando persistir **TZDEFINITION** em um fluxo para compromisso com uma propriedade binária, como **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="296d2-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="296d2-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="296d2-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="296d2-126">**dispidApptTZDefEndDisplay** especifica informações de fuso horário para a **propriedade dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="296d2-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="296d2-127">O formato, as restrições e a computação de **dispidApptTZDefEndDisplay** são os mesmos especificados na **propriedade dispidApptTZDefStartDisplay.**</span><span class="sxs-lookup"><span data-stu-id="296d2-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="296d2-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="296d2-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="296d2-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="296d2-129">Protocol specifications</span></span>

<span data-ttu-id="296d2-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296d2-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296d2-131">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="296d2-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="296d2-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="296d2-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="296d2-133">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="296d2-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="296d2-134">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="296d2-134">Header files</span></span>

<span data-ttu-id="296d2-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="296d2-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="296d2-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="296d2-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="296d2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="296d2-137">See also</span></span>



[<span data-ttu-id="296d2-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="296d2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="296d2-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="296d2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="296d2-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="296d2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="296d2-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="296d2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


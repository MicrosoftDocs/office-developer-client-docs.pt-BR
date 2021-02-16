---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionStartDispl
api_type:
- COM
ms.assetid: 08239670-3211-420c-99d7-0056ed967cb8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 504dc4b1cecb9798590e4a15968acc3aa98fe4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345014"
---
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="95a19-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="95a19-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="95a19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95a19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95a19-105">Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que armazena a descrição para o fuso horário que é usado quando a hora de início de um compromisso de instância única ou solicitação de reunião é selecionada.</span><span class="sxs-lookup"><span data-stu-id="95a19-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95a19-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="95a19-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="95a19-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="95a19-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="95a19-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="95a19-108">Property set:</span></span>  <br/> |<span data-ttu-id="95a19-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="95a19-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="95a19-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="95a19-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="95a19-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="95a19-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="95a19-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="95a19-112">Data type:</span></span>  <br/> |<span data-ttu-id="95a19-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="95a19-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="95a19-114">Área:</span><span class="sxs-lookup"><span data-stu-id="95a19-114">Area:</span></span>  <br/> |<span data-ttu-id="95a19-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="95a19-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95a19-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="95a19-116">Remarks</span></span>

<span data-ttu-id="95a19-117">Microsoft Office Outlook 2003 ou anterior, e soluções baseadas no CDO (Collaboration Data Objects) 1.2.1 e que não executaram a ferramenta de atualização de calendário para o Outlook ou o Microsoft Exchange Server, armazene a hora de início e a hora de término de compromissos de instância única e solicitações de reunião em TEMPO Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="95a19-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="95a19-118">Esses clientes não armazenam informações para o fuso horário no qual a solicitação de compromisso ou reunião é criada.</span><span class="sxs-lookup"><span data-stu-id="95a19-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="95a19-119">As versões do Outlook desde o Microsoft Office Outlook 2007 e as soluções baseadas no CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam essa propriedade para armazenar o fuso horário para a hora de início.</span><span class="sxs-lookup"><span data-stu-id="95a19-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="95a19-120">A **propriedade dispidApptTZDefStartDisplay** mostra o compromisso ou a reunião no fuso horário original que foi agendado.</span><span class="sxs-lookup"><span data-stu-id="95a19-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="95a19-121">Ele determina se a hora de início deve ser ajustada se as regras do fuso horário mudarem.</span><span class="sxs-lookup"><span data-stu-id="95a19-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="95a19-122">Se essa propriedade estiver ausente, o fuso horário local atual será assumido.</span><span class="sxs-lookup"><span data-stu-id="95a19-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="95a19-123">Essa propriedade é usada apenas para fins de exibição e não é usada na expansão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="95a19-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="95a19-124">Um analisador deve ter cuidado ao ler um fluxo obtido dessa propriedade ou quando persistir **TZDEFINITION** em um fluxo para compromisso com uma propriedade binária, como **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="95a19-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="95a19-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="95a19-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="95a19-126">Esta propriedade especifica informações de fuso horário para **a propriedade dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="95a19-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="95a19-127">O valor de **dispidApptTZDefStartDisplay** é usado para converter a data e a hora de início de UTC no fuso horário local para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="95a19-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="95a19-128">Para cada **TZRULE** especificado por essa propriedade, o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="95a19-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="95a19-129">Por exemplo, se **o TZRULE** for a regra efetiva, o valor do campo, **TZRULE** deverá ser "0x0002"; caso contrário, ele deve ser "0x0000".</span><span class="sxs-lookup"><span data-stu-id="95a19-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="95a19-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="95a19-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="95a19-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="95a19-131">Protocol specifications</span></span>

<span data-ttu-id="95a19-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95a19-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95a19-133">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="95a19-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="95a19-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="95a19-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="95a19-135">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="95a19-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="95a19-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="95a19-136">Header files</span></span>

<span data-ttu-id="95a19-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="95a19-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="95a19-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="95a19-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95a19-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="95a19-139">See also</span></span>



[<span data-ttu-id="95a19-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="95a19-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="95a19-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="95a19-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="95a19-142">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="95a19-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="95a19-143">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="95a19-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


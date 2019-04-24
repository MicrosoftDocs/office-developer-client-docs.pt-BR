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
# <a name="pidlidappointmenttimezonedefinitionstartdisplay-canonical-property"></a><span data-ttu-id="fcd80-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionStartDisplay</span><span class="sxs-lookup"><span data-stu-id="fcd80-103">PidLidAppointmentTimeZoneDefinitionStartDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="fcd80-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcd80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcd80-105">Contém um Stream que mapeia para o formato persistente de uma estrutura [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição do fuso horário usado quando o horário de início de um compromisso ou solicitação de reunião de instância única é selecionado.</span><span class="sxs-lookup"><span data-stu-id="fcd80-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the start time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcd80-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fcd80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fcd80-107">dispidApptTZDefStartDisplay</span><span class="sxs-lookup"><span data-stu-id="fcd80-107">dispidApptTZDefStartDisplay</span></span>  <br/> |
|<span data-ttu-id="fcd80-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="fcd80-108">Property set:</span></span>  <br/> |<span data-ttu-id="fcd80-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fcd80-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fcd80-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="fcd80-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fcd80-111">0x0000825E</span><span class="sxs-lookup"><span data-stu-id="fcd80-111">0x0000825E</span></span>  <br/> |
|<span data-ttu-id="fcd80-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fcd80-112">Data type:</span></span>  <br/> |<span data-ttu-id="fcd80-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fcd80-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fcd80-114">Área:</span><span class="sxs-lookup"><span data-stu-id="fcd80-114">Area:</span></span>  <br/> |<span data-ttu-id="fcd80-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="fcd80-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcd80-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fcd80-116">Remarks</span></span>

<span data-ttu-id="fcd80-117">Microsoft Office Outlook 2003 ou anterior, e soluções baseadas em Collaboration Data Objects (CDO) 1.2.1 e que não executaram a ferramenta de atualização de calendário para Outlook ou Microsoft Exchange Server, armazenam a hora de início e a hora de término de uma única instância compromissos e solicitações de reunião no tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="fcd80-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fcd80-118">Esses clientes não armazenam informações sobre o fuso horário em que o compromisso ou solicitação de reunião foi criado.</span><span class="sxs-lookup"><span data-stu-id="fcd80-118">These clients do not store any information for the time zone in which the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="fcd80-119">Versões do Outlook desde o Microsoft Office Outlook 2007 e soluções baseadas no CDO 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam essa propriedade para armazenar o fuso horário para a hora de início.</span><span class="sxs-lookup"><span data-stu-id="fcd80-119">Versions of Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use this property to store the time zone for the start time.</span></span> <span data-ttu-id="fcd80-120">A propriedade **dispidApptTZDefStartDisplay** mostra o compromisso ou a reunião no fuso horário original em que foi agendado.</span><span class="sxs-lookup"><span data-stu-id="fcd80-120">The **dispidApptTZDefStartDisplay** property shows the appointment or meeting in the original time zone that it was scheduled.</span></span> <span data-ttu-id="fcd80-121">Ele determina se a hora de início deve ser ajustada se as regras do fuso horário forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="fcd80-121">It determines whether the start time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="fcd80-122">Se essa propriedade estiver ausente, será considerado o fuso horário local atual.</span><span class="sxs-lookup"><span data-stu-id="fcd80-122">If this property is missing, the current local time zone is assumed.</span></span> <span data-ttu-id="fcd80-123">Essa propriedade é usada apenas para fins de exibição e não é usada em expansão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="fcd80-123">This property is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="fcd80-124">Um analisador deve ser cuidadoso quando lê um fluxo obtido dessa propriedade ou quando ele persiste **TZDEFINITION** para um Stream de compromisso para uma propriedade binária, como **dispidApptTZDefStartDisplay**.</span><span class="sxs-lookup"><span data-stu-id="fcd80-124">A parser must be careful when it reads a stream obtained from this property, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefStartDisplay**.</span></span> <span data-ttu-id="fcd80-125">Para obter mais informações, consulte [sobre a persistência de TZDEFINITION em um Stream para confirmar uma propriedade binária](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fcd80-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="fcd80-126">Esta propriedade especifica informações de fuso horário para a propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="fcd80-126">This property specifies time zone information for the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="fcd80-127">O valor de **dispidApptTZDefStartDisplay** é usado para converter a data de início e a hora do UTC para o fuso horário local para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="fcd80-127">The value of **dispidApptTZDefStartDisplay** is used to convert the start date and time from UTC to the local time zone for display purposes.</span></span> <span data-ttu-id="fcd80-128">Para cada **TZRULE** especificado por essa propriedade, o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="fcd80-128">For each **TZRULE** specified by this property, the TZRULE_FLAG_RECUR_CURRENT_TZREG flag must not be set.</span></span> <span data-ttu-id="fcd80-129">Por exemplo, se **TZRULE** for a regra efetiva, o valor do campo **TZRULE** deverá ser "0x0002"; caso contrário, ele deve ser "0x0000".</span><span class="sxs-lookup"><span data-stu-id="fcd80-129">For example, if the **TZRULE** is the effective rule, the value of the field, **TZRULE** must be "0x0002"; otherwise, it must be "0x0000".</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fcd80-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fcd80-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fcd80-131">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="fcd80-131">Protocol specifications</span></span>

<span data-ttu-id="fcd80-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcd80-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcd80-133">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas..</span><span class="sxs-lookup"><span data-stu-id="fcd80-133">Provides property set definitions and references to related Exchange Server protocol specifications..</span></span>
    
<span data-ttu-id="fcd80-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fcd80-134">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fcd80-135">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fcd80-135">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fcd80-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fcd80-136">Header files</span></span>

<span data-ttu-id="fcd80-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fcd80-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="fcd80-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fcd80-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fcd80-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcd80-139">See also</span></span>



[<span data-ttu-id="fcd80-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fcd80-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fcd80-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fcd80-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fcd80-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fcd80-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fcd80-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fcd80-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


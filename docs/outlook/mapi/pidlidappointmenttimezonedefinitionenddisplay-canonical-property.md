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
ms.openlocfilehash: facbcb9eed18db304cac334be845c0b3869ba508
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574801"
---
# <a name="pidlidappointmenttimezonedefinitionenddisplay-canonical-property"></a><span data-ttu-id="ca013-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionEndDisplay</span><span class="sxs-lookup"><span data-stu-id="ca013-103">PidLidAppointmentTimeZoneDefinitionEndDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="ca013-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca013-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca013-105">Contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição para o fuso horário que é usado quando a hora de término de uma única instância compromisso ou solicitação de reunião é selecionada.</span><span class="sxs-lookup"><span data-stu-id="ca013-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when the end time of a single-instance appointment or meeting request is selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca013-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ca013-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca013-107">dispidApptTZDefEndDisplay</span><span class="sxs-lookup"><span data-stu-id="ca013-107">dispidApptTZDefEndDisplay</span></span>  <br/> |
|<span data-ttu-id="ca013-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="ca013-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca013-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ca013-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ca013-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="ca013-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca013-111">0x0000825F</span><span class="sxs-lookup"><span data-stu-id="ca013-111">0x0000825F</span></span>  <br/> |
|<span data-ttu-id="ca013-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ca013-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca013-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ca013-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ca013-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ca013-114">Area:</span></span>  <br/> |<span data-ttu-id="ca013-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="ca013-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca013-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca013-116">Remarks</span></span>

<span data-ttu-id="ca013-117">Microsoft Office Outlook 2003 ou anterior e soluções que são baseados em Collaboration Data Objects (CDO) 1.2.1 e que não têm executar a ferramenta de atualização de calendário do Outlook ou o Microsoft Exchange Server, para armazenar a hora de início e hora de término de ocorrência única compromissos e solicitações de reunião no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="ca013-117">Microsoft Office Outlook 2003 or earlier, and solutions that are based on Collaboration Data Objects (CDO) 1.2.1 and that have not run the calendar update tool for Outlook or Microsoft Exchange Server, store the start time and end time of single-instance appointments and meeting requests in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ca013-118">Esses clientes não armazene qualquer informação para o fuso horário em que a solicitação de reunião ou compromisso é criada.</span><span class="sxs-lookup"><span data-stu-id="ca013-118">These clients do not store any information for the time zone where the appointment or meeting request is created.</span></span>
  
<span data-ttu-id="ca013-119">Versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e soluções com base no CDO 1.2.1 que executaram o calendário do Outlook ou o Exchange Server atualizar de uso de ferramenta **dispidApptTZDefEndDisplay** para armazenar o fuso horário para a hora de término.</span><span class="sxs-lookup"><span data-stu-id="ca013-119">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on CDO 1.2.1 that have run the Outlook or Exchange Server calendar update tool use **dispidApptTZDefEndDisplay** to store the time zone for the end time.</span></span> <span data-ttu-id="ca013-120">**dispidApptTZDefEndDisplay** mostra o compromisso ou reunião no fuso horário original que ele estava agendado e determina se a hora de término deve ser ajustada se alterar as regras do fuso horário.</span><span class="sxs-lookup"><span data-stu-id="ca013-120">**dispidApptTZDefEndDisplay** shows the appointment or meeting in the original time zone that it was scheduled, and determines whether the end time should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="ca013-121">Se essa propriedade estiver ausente, o fuso horário especificado pela propriedade **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) é usado.</span><span class="sxs-lookup"><span data-stu-id="ca013-121">If this property is missing, the time zone specified by the **dispidApptTZDefStartDisplay** ([PidLidAppointmentTimeZoneDefinitionStartDisplay](pidlidappointmenttimezonedefinitionstartdisplay-canonical-property.md)) property is used.</span></span> <span data-ttu-id="ca013-122">Se **dispidApptTZDefStartDisplay** estiver ausente ou inválido, o fuso horário local atual é assumido.</span><span class="sxs-lookup"><span data-stu-id="ca013-122">If **dispidApptTZDefStartDisplay** is missing or invalid, the current local time zone is assumed.</span></span> <span data-ttu-id="ca013-123">**dispidApptTZDefEndDisplay** é usado somente para exibição e não é usado na expansão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="ca013-123">**dispidApptTZDefEndDisplay** is used for display purposes only and is not used in recurrence expansion.</span></span> 
  
<span data-ttu-id="ca013-124">Um analisador deve tomar cuidado quando ele lê um stream obtido de **dispidApptTZDefEndDisplay**ou quando ele persiste **TZDEFINITION** a um fluxo de compromisso em uma propriedade binária como **dispidApptTZDefEndDisplay**.</span><span class="sxs-lookup"><span data-stu-id="ca013-124">A parser must be careful when it reads a stream obtained from **dispidApptTZDefEndDisplay**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefEndDisplay**.</span></span> <span data-ttu-id="ca013-125">Para obter mais informações, consulte [About TZDEFINITION mantendo a um fluxo de confirmar uma propriedade binária](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ca013-125">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="ca013-126">**dispidApptTZDefEndDisplay** Especifica as informações de fuso horário para a propriedade **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ca013-126">**dispidApptTZDefEndDisplay** specifies time zone information for the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="ca013-127">O formato, restrições e computação do **dispidApptTZDefEndDisplay** são os mesmos conforme especificado na propriedade **dispidApptTZDefStartDisplay** .</span><span class="sxs-lookup"><span data-stu-id="ca013-127">The format, constraints, and computation of **dispidApptTZDefEndDisplay** are the same as specified in the **dispidApptTZDefStartDisplay** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ca013-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca013-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca013-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ca013-129">Protocol specifications</span></span>

<span data-ttu-id="ca013-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca013-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca013-131">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ca013-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca013-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca013-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca013-133">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="ca013-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca013-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ca013-134">Header files</span></span>

<span data-ttu-id="ca013-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca013-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca013-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ca013-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca013-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca013-137">See also</span></span>



[<span data-ttu-id="ca013-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ca013-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca013-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ca013-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca013-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ca013-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca013-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ca013-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


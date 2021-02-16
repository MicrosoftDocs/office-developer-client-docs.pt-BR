---
title: Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentTimeZoneDefinitionRecur
api_type:
- COM
ms.assetid: 52fd57a0-9e34-4452-9ecd-2acb454446c9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5e9b06178a1517fc1c8652b0d667faf1afc77cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345350"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="feac5-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="feac5-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="feac5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="feac5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="feac5-105">Contém um fluxo que é mapeado para o formato persistente de uma estrutura [TZDEFINITION,](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) que armazena a descrição para o fuso horário que é usado quando uma solicitação de reunião ou compromisso recorrente é criada.</span><span class="sxs-lookup"><span data-stu-id="feac5-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](https://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="feac5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="feac5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="feac5-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="feac5-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="feac5-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="feac5-108">Property set:</span></span>  <br/> |<span data-ttu-id="feac5-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="feac5-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="feac5-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="feac5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="feac5-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="feac5-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="feac5-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="feac5-112">Data type:</span></span>  <br/> |<span data-ttu-id="feac5-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="feac5-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="feac5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="feac5-114">Area:</span></span>  <br/> |<span data-ttu-id="feac5-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="feac5-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="feac5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="feac5-116">Remarks</span></span>

<span data-ttu-id="feac5-117">As versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e as soluções baseadas no CDO (Collaboration Data Objects) 1.2.1 que executaram a ferramenta de atualização de calendário do Outlook ou do Exchange Server usam as propriedades **dispidApptTZDefRecur** e **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar se a reunião recorrente deve ser ajustada se as regras do fuso horário mudarem.</span><span class="sxs-lookup"><span data-stu-id="feac5-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="feac5-118">Essas propriedades devem ser sincronizadas, pois os clientes mais antigos ainda podem manipular a **propriedade dispidTimeZoneStruct.**</span><span class="sxs-lookup"><span data-stu-id="feac5-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="feac5-119">Para detectar se as duas propriedades estão sincronizadas, o membro **wFlags** da regra que corresponde **a dispidTimeZoneStruct** deve ter o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG definido.</span><span class="sxs-lookup"><span data-stu-id="feac5-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="feac5-120">Se esse sinalizador não estiver definido ou estiver definido e a regra na propriedade **dispidTimeZoneStruct** não corresponder à regra marcada, a propriedade **dispidApptTZDefRecur** deverá ser descartada e **dispidTimeZoneStruct** deverá ser usada.</span><span class="sxs-lookup"><span data-stu-id="feac5-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="feac5-121">Quando você escreve as propriedades **dispidApptTZDefRecur** e **dispidTimeZoneStruct** em uma nova reunião recorrente ou, quando você faz uma escolha arbitrária para usar a propriedade **dispidTimeZoneStruct,** a definição atual para o fuso horário (de acordo com o Registro do Windows) deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="feac5-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="feac5-122">Um analisador deve ter cuidado ao ler um fluxo obtido de **dispidApptTZDefRecur** ou quando persistir **TZDEFINITION** para um fluxo para compromisso com uma propriedade binária, como **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="feac5-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="feac5-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="feac5-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](https://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="feac5-124">**dispidApptTZDefRecur** especifica informações de fuso horário que descrevem como converter a data e a hora da reunião em uma série recorrente de e para UTC (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="feac5-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="feac5-125">Se essa propriedade estiver definida, mas tiver dados inconsistentes com os dados representados por **dispidTimeZoneStruct**, o cliente deverá usar **dispidTimeZoneStruct** em vez de **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="feac5-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="feac5-126">Se **dispidApptTZDefRecur** não estiver definida, a propriedade **PidLidTimeZoneStruct** será usada.</span><span class="sxs-lookup"><span data-stu-id="feac5-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="feac5-127">Os campos neste BLOB são codificados em ordem de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="feac5-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="feac5-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="feac5-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="feac5-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="feac5-129">Protocol specifications</span></span>

<span data-ttu-id="feac5-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feac5-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feac5-131">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="feac5-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="feac5-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="feac5-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="feac5-133">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="feac5-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="feac5-134">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="feac5-134">Header files</span></span>

<span data-ttu-id="feac5-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="feac5-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="feac5-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="feac5-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="feac5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="feac5-137">See also</span></span>



[<span data-ttu-id="feac5-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="feac5-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="feac5-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="feac5-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="feac5-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="feac5-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="feac5-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="feac5-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.openlocfilehash: 5cff6ec7b39c26eec098d250688d98bf1e4799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768329"
---
# <a name="pidlidappointmenttimezonedefinitionrecur-canonical-property"></a><span data-ttu-id="4873e-103">Propriedade canônica PidLidAppointmentTimeZoneDefinitionRecur</span><span class="sxs-lookup"><span data-stu-id="4873e-103">PidLidAppointmentTimeZoneDefinitionRecur Canonical Property</span></span>

  
  
<span data-ttu-id="4873e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4873e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4873e-105">Contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) , que armazena a descrição para o fuso horário que é usado quando uma solicitação de reunião ou um compromisso recorrente é criada.</span><span class="sxs-lookup"><span data-stu-id="4873e-105">Contains a stream that maps to the persisted format of a [TZDEFINITION](http://msdn.microsoft.com/library/0ae21571-2299-6407-807c-428668bb6798%28Office.15%29.aspx) structure, which stores the description for the time zone that is used when a recurring appointment or meeting request is created.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4873e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4873e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4873e-107">dispidApptTZDefRecur</span><span class="sxs-lookup"><span data-stu-id="4873e-107">dispidApptTZDefRecur</span></span>  <br/> |
|<span data-ttu-id="4873e-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4873e-108">Property set:</span></span>  <br/> |<span data-ttu-id="4873e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="4873e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="4873e-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4873e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4873e-111">0x00008260</span><span class="sxs-lookup"><span data-stu-id="4873e-111">0x00008260</span></span>  <br/> |
|<span data-ttu-id="4873e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4873e-112">Data type:</span></span>  <br/> |<span data-ttu-id="4873e-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4873e-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4873e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4873e-114">Area:</span></span>  <br/> |<span data-ttu-id="4873e-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="4873e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4873e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4873e-116">Remarks</span></span>

<span data-ttu-id="4873e-117">Versões do Microsoft Outlook desde o Microsoft Office Outlook 2007 e soluções baseadas em Collaboration Data Objects (CDO) 1.2.1 que executaram o calendário do Outlook ou o Exchange Server atualizar o uso da ferramenta de **dispidApptTZDefRecur** e ** dispidTimeZoneStruct** propriedades ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) para determinar se a reunião recorrente deve ser ajustada se alterar as regras do fuso horário.</span><span class="sxs-lookup"><span data-stu-id="4873e-117">Versions of Microsoft Outlook since Microsoft Office Outlook 2007, and solutions based on Collaboration Data Objects (CDO) 1.2.1 that have run the Outlook or Exchange Server calendar update tool use the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** ([PidLidTimeZoneStruct](pidlidtimezonestruct-canonical-property.md)) properties to determine whether the recurring meeting should be adjusted if the rules of the time zone change.</span></span> <span data-ttu-id="4873e-118">Essas propriedades devem ser sincronizadas, pois clientes mais antigos ainda podem manipular a propriedade **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="4873e-118">These properties must be synchronized, because older clients may still manipulate the **dispidTimeZoneStruct** property.</span></span> <span data-ttu-id="4873e-119">Para detectar se as duas propriedades são sincronizadas, o membro **wFlags** para a regra que corresponde a **dispidTimeZoneStruct** deve ter o sinalizador TZRULE_FLAG_RECUR_CURRENT_TZREG definido.</span><span class="sxs-lookup"><span data-stu-id="4873e-119">To detect whether the two properties are synchronized, the **wFlags** member for the rule that matches **dispidTimeZoneStruct** should have the TZRULE_FLAG_RECUR_CURRENT_TZREG flag set.</span></span> <span data-ttu-id="4873e-120">Se esse sinalizador não estiver definida, ou seja definido e a regra na propriedade **dispidTimeZoneStruct** não coincide com a regra marcada, a propriedade **dispidApptTZDefRecur** deverão ser descartada e **dispidTimeZoneStruct** deve ser usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4873e-120">If this flag is not set, or it is set and the rule in the **dispidTimeZoneStruct** property does not match the marked rule, the **dispidApptTZDefRecur** property should be discarded and **dispidTimeZoneStruct** should be used instead.</span></span> 
  
<span data-ttu-id="4873e-121">Quando você escreve **dispidApptTZDefRecur** tanto o **dispidTimeZoneStruct** propriedades para uma nova reunião recorrente ou, quando você faz uma opção arbitrária para usar a propriedade **dispidTimeZoneStruct** , a definição atual para o (de fuso horário de acordo com o registro do Windows) deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="4873e-121">When you write both the **dispidApptTZDefRecur** and **dispidTimeZoneStruct** properties to a new recurring meeting, or, when you make an arbitrary choice to use the **dispidTimeZoneStruct** property, the current definition for the time zone (according to the Windows registry) should be used.</span></span> 
  
<span data-ttu-id="4873e-122">Um analisador deve tomar cuidado quando ele lê um fluxo que for obtido de **dispidApptTZDefRecur**ou quando ele persiste **TZDEFINITION** a um fluxo de compromisso em uma propriedade binária como **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="4873e-122">A parser must be careful when it reads a stream that is obtained from **dispidApptTZDefRecur**, or when it persists **TZDEFINITION** to a stream for commitment to a binary property such as **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="4873e-123">Para obter mais informações, consulte [About TZDEFINITION mantendo a um fluxo de confirmar uma propriedade binária](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4873e-123">For more information, see [About persisting TZDEFINITION to a stream to commit to a binary property](http://msdn.microsoft.com/library/0dec535d-d48f-39a5-97d5-0bd109134b3b%28Office.15%29.aspx).</span></span>
  
 <span data-ttu-id="4873e-124">**dispidApptTZDefRecur** Especifica as informações de fuso horário que descrevem como converter a data da reunião e a hora em uma série recorrente para e do tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="4873e-124">**dispidApptTZDefRecur** specifies time zone information that describes how to convert the meeting date and time on a recurring series to and from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="4873e-125">Se essa propriedade estiver definida, mas ela tem dados inconsistente com os dados representados pela **dispidTimeZoneStruct**, o cliente deve usar **dispidTimeZoneStruct** em vez de **dispidApptTZDefRecur**.</span><span class="sxs-lookup"><span data-stu-id="4873e-125">If this property is set but it has data that is inconsistent with the data represented by **dispidTimeZoneStruct**, the client must use **dispidTimeZoneStruct** instead of **dispidApptTZDefRecur**.</span></span> <span data-ttu-id="4873e-126">Se **dispidApptTZDefRecur** não estiver definida, a propriedade **PidLidTimeZoneStruct** será usada.</span><span class="sxs-lookup"><span data-stu-id="4873e-126">If **dispidApptTZDefRecur** is not set, the **PidLidTimeZoneStruct** property will be used instead.</span></span> <span data-ttu-id="4873e-127">Os campos neste BLOB são codificados em ordem de bytes endian pouco.</span><span class="sxs-lookup"><span data-stu-id="4873e-127">The fields in this BLOB are encoded in little-endian byte order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4873e-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4873e-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4873e-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4873e-129">Protocol specifications</span></span>

<span data-ttu-id="4873e-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4873e-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4873e-131">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4873e-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4873e-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4873e-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4873e-133">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="4873e-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4873e-134">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4873e-134">Header files</span></span>

<span data-ttu-id="4873e-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4873e-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="4873e-136">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4873e-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4873e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4873e-137">See also</span></span>



[<span data-ttu-id="4873e-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4873e-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4873e-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4873e-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4873e-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4873e-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4873e-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4873e-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a1a96cdb3aed03b9621097f1ef858a09391c0693
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768738"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="a0dab-103">Propriedade canônica PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="a0dab-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="a0dab-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0dab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0dab-105">Contém um stream que mapeie para o formato persistente de uma estrutura [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) , que descreve o fuso horário a ser usado para a hora de início e término de uma solicitação de reunião ou um compromisso recorrente.</span><span class="sxs-lookup"><span data-stu-id="a0dab-105">Contains a stream that maps to the persisted format of a [TZREG](http://msdn.microsoft.com/en-us/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0dab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a0dab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0dab-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="a0dab-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="a0dab-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="a0dab-108">Property set:</span></span>  <br/> |<span data-ttu-id="a0dab-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="a0dab-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="a0dab-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="a0dab-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a0dab-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="a0dab-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="a0dab-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a0dab-112">Data type:</span></span>  <br/> |<span data-ttu-id="a0dab-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a0dab-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a0dab-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a0dab-114">Area:</span></span>  <br/> |<span data-ttu-id="a0dab-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="a0dab-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0dab-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0dab-116">Remarks</span></span>

<span data-ttu-id="a0dab-117">Microsoft Office Outlook 2003, versões anteriores do Outlook e aplicativos que se baseiam em Collaboration Data Objects (CDO) 1.21 cujos usuários não executou a ferramenta de atualização de calendário fornecida pelo Outlook ou o Exchange Server armazenam a hora de início e a hora de término de um recorrente compromisso ou uma solicitação de reunião, como tempo relativo e armazene o fuso horário em que a solicitação de reunião ou compromisso é criada no **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="a0dab-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="a0dab-118">No entanto, esse esquema ignora que ao longo do tempo, as regras de fuso horário podem mudar, resultando em alguns compromissos e reuniões que os usuários agendado antes que as regras alteradas e ocorrerem em momentos incorretos.</span><span class="sxs-lookup"><span data-stu-id="a0dab-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="a0dab-119">Usuários e administradores que não estejam executando o Windows Vista ou que não têm atualizações automáticas ativadas devem usar o calendário a alteração da Base de ferramentas que são fornecidas pelo Outlook ou o Exchange Server para ajustar o tempo de tais compromissos e solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="a0dab-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="a0dab-120">Para obter mais informações sobre essas ferramentas de REBASE de calendário e APIs que alterar a calendários base, consulte [About REBASE de calendários programaticamente para o horário de verão](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dab-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](http://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="a0dab-121">Use o seguinte formato de pouca-endian durante a análise de um stream obtido a partir de **dispidTimeZoneStruct**ou quando mantendo a estrutura **TZREG** a um fluxo para comprometer à propriedade **dispidTimeZoneStruct** binário.</span><span class="sxs-lookup"><span data-stu-id="a0dab-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="a0dab-122">Essa propriedade for definida em uma série recorrente para especificar informações de fuso horário e especifica como converter os campos de hora entre hora local e o tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="a0dab-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a0dab-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0dab-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0dab-124">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a0dab-124">Protocol specifications</span></span>

<span data-ttu-id="a0dab-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dab-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dab-126">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a0dab-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0dab-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0dab-127">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0dab-128">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="a0dab-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0dab-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0dab-129">Header files</span></span>

<span data-ttu-id="a0dab-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a0dab-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0dab-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a0dab-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0dab-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0dab-132">See also</span></span>



[<span data-ttu-id="a0dab-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a0dab-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0dab-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a0dab-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0dab-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a0dab-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0dab-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a0dab-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


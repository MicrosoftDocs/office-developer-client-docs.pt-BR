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
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346372"
---
# <a name="pidlidtimezonestruct-canonical-property"></a><span data-ttu-id="54862-103">Propriedade canônica PidLidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="54862-103">PidLidTimeZoneStruct Canonical Property</span></span>

  
  
<span data-ttu-id="54862-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54862-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54862-105">Contém um Stream que mapeia para o formato persistente de uma estrutura [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , que descreve o fuso horário a ser usado para a hora de início e de término de um compromisso recorrente ou uma solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="54862-105">Contains a stream that maps to the persisted format of a [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) structure, which describes the time zone to be used for the start and end time of a recurring appointment or meeting request.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54862-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="54862-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54862-107">dispidTimeZoneStruct</span><span class="sxs-lookup"><span data-stu-id="54862-107">dispidTimeZoneStruct</span></span>  <br/> |
|<span data-ttu-id="54862-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="54862-108">Property set:</span></span>  <br/> |<span data-ttu-id="54862-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="54862-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="54862-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="54862-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="54862-111">0x00008233</span><span class="sxs-lookup"><span data-stu-id="54862-111">0x00008233</span></span>  <br/> |
|<span data-ttu-id="54862-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="54862-112">Data type:</span></span>  <br/> |<span data-ttu-id="54862-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="54862-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="54862-114">Área:</span><span class="sxs-lookup"><span data-stu-id="54862-114">Area:</span></span>  <br/> |<span data-ttu-id="54862-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="54862-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54862-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54862-116">Remarks</span></span>

<span data-ttu-id="54862-117">Microsoft Office Outlook 2003, versões anteriores do Outlook e aplicativos baseados em Collaboration Data Objects (CDO) 1,21 cujos usuários não executaram a ferramenta de atualização de calendário fornecida pelo Outlook ou pelo Exchange Server Store a hora de início e a hora de término de um compromisso recorrente ou solicitação de reunião como tempo relativo e armazene o fuso horário em que o compromisso ou solicitação de reunião é criado no **dispidTimeZoneStruct**.</span><span class="sxs-lookup"><span data-stu-id="54862-117">Microsoft Office Outlook 2003, earlier versions of Outlook, and applications that are based on Collaboration Data Objects (CDO) 1.21 whose users have not run the calendar update tool provided by Outlook or Exchange Server store the start time and end time of a recurring appointment or meeting request as relative time, and store the time zone where the appointment or meeting request is created in **dispidTimeZoneStruct**.</span></span> <span data-ttu-id="54862-118">No enTanto, esse esquema ignora isso com o tempo, as regras de fuso horário podem ser alteradas, resultando em alguns compromissos e reuniões que os usuários agendados antes que as regras sejam alteradas e ocorram em horários incorretos.</span><span class="sxs-lookup"><span data-stu-id="54862-118">However, this scheme ignores that over time, time zone rules can change, resulting in some appointments and meetings that users scheduled before the rules changed and occur at incorrect times.</span></span> <span data-ttu-id="54862-119">Os usuários e administradores que não estão executando o Windows Vista ou que não têm as atualizações automáticas ativadas devem usar as ferramentas de alteração de base de calendário fornecidas pelo Outlook ou pelo Exchange Server para ajustar o tempo desses compromissos e solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="54862-119">Users and administrators who are not running Windows Vista or who do not have automatic updates turned on should use the calendar rebasing tools that are provided by Outlook or Exchange Server to adjust the time of such appointments and meeting requests.</span></span> <span data-ttu-id="54862-120">Para obter mais informações sobre essas ferramentas e APIs de alteração da base de calendário, consulte sobre como rebasear calendários programaticamente [para horário de verão](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54862-120">For more information about these calendar rebasing tools and APIs that rebase calendars, see [About rebasing calendars programmatically for Daylight Saving Time](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)</span></span>
  
<span data-ttu-id="54862-121">Use o seguinte formato little-endian ao analisar um Stream obtido do **dispidTimeZoneStruct**ou quando persistir a estrutura do **TZREG** em um Stream para confirmar a propriedade binária **dispidTimeZoneStruct** .</span><span class="sxs-lookup"><span data-stu-id="54862-121">Use the following little-endian format when parsing a stream obtained from **dispidTimeZoneStruct**, or when persisting the **TZREG** structure to a stream to commit to the **dispidTimeZoneStruct** binary property.</span></span> 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

<span data-ttu-id="54862-122">Essa propriedade é definida em uma série recorrente para especificar informações de fuso horário e especifica como converter campos de hora entre o horário local e o UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="54862-122">This property is set on a recurring series to specify time-zone information, and specifies how to convert time fields between local time and Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="54862-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54862-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54862-124">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="54862-124">Protocol specifications</span></span>

<span data-ttu-id="54862-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54862-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54862-126">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="54862-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54862-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54862-127">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54862-128">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="54862-128">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54862-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54862-129">Header files</span></span>

<span data-ttu-id="54862-130">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="54862-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="54862-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="54862-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54862-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="54862-132">See also</span></span>



[<span data-ttu-id="54862-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54862-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54862-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="54862-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54862-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="54862-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54862-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="54862-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


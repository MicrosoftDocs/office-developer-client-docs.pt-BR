---
title: Propriedade canônica PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319268"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="6c354-103">Propriedade canônica PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="6c354-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="6c354-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c354-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c354-105">Especifica informações sobre o fuso horário de uma reunião recorrente.</span><span class="sxs-lookup"><span data-stu-id="6c354-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c354-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6c354-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c354-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="6c354-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="6c354-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="6c354-108">Property set:</span></span>  <br/> |<span data-ttu-id="6c354-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="6c354-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="6c354-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6c354-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c354-111">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="6c354-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="6c354-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6c354-112">Data type:</span></span>  <br/> |<span data-ttu-id="6c354-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c354-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c354-114">Área:</span><span class="sxs-lookup"><span data-stu-id="6c354-114">Area:</span></span>  <br/> |<span data-ttu-id="6c354-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="6c354-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c354-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c354-116">Remarks</span></span>

<span data-ttu-id="6c354-117">Essa propriedade só será lida se a propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) não estiver definida, mas se a propriedade **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) for true e **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) é false.</span><span class="sxs-lookup"><span data-stu-id="6c354-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="6c354-118">A palavra inferior Especifica um índice em uma tabela que contém informações de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="6c354-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="6c354-119">Na palavra superior, apenas o bit mais alto é lido.</span><span class="sxs-lookup"><span data-stu-id="6c354-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="6c354-120">Se esse bit for definido, o fuso horário mencionado não irá observar o horário de Verão (DST), caso contrário, as datas de horário de verão detalhadas em [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) serão seguidas.</span><span class="sxs-lookup"><span data-stu-id="6c354-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c354-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c354-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c354-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="6c354-122">Protocol specifications</span></span>

<span data-ttu-id="6c354-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c354-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c354-124">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6c354-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c354-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c354-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c354-126">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="6c354-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c354-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c354-127">Header files</span></span>

<span data-ttu-id="6c354-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6c354-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c354-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6c354-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c354-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c354-130">See also</span></span>



[<span data-ttu-id="6c354-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c354-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c354-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="6c354-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c354-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c354-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c354-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6c354-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


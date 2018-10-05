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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389922"
---
# <a name="pidlidtimezone-canonical-property"></a><span data-ttu-id="94f97-103">Propriedade canônica PidLidTimeZone</span><span class="sxs-lookup"><span data-stu-id="94f97-103">PidLidTimeZone Canonical Property</span></span>

  
  
<span data-ttu-id="94f97-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94f97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94f97-105">Especifica informações sobre o fuso horário de uma reunião recorrente.</span><span class="sxs-lookup"><span data-stu-id="94f97-105">Specifies information about the time zone of a recurring meeting.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="94f97-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="94f97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="94f97-107">LID_TIME_ZONE</span><span class="sxs-lookup"><span data-stu-id="94f97-107">LID_TIME_ZONE</span></span>  <br/> |
|<span data-ttu-id="94f97-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="94f97-108">Property set:</span></span>  <br/> |<span data-ttu-id="94f97-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="94f97-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="94f97-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="94f97-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="94f97-111">0x0000000c</span><span class="sxs-lookup"><span data-stu-id="94f97-111">0x0000000C</span></span>  <br/> |
|<span data-ttu-id="94f97-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="94f97-112">Data type:</span></span>  <br/> |<span data-ttu-id="94f97-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="94f97-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="94f97-114">Área:</span><span class="sxs-lookup"><span data-stu-id="94f97-114">Area:</span></span>  <br/> |<span data-ttu-id="94f97-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="94f97-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="94f97-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="94f97-116">Remarks</span></span>

<span data-ttu-id="94f97-117">Essa propriedade é somente leitura se a propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) não estiver definida, mas se a propriedade **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) for TRUE e **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) propriedade for FALSE.</span><span class="sxs-lookup"><span data-stu-id="94f97-117">This property is only read if the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property is not set, but if the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property is TRUE and the **LID_IS_EXCEPTION** ([PidLidIsException](pidlidisexception-canonical-property.md)) property is FALSE.</span></span> <span data-ttu-id="94f97-118">A palavra inferior Especifica um índice em uma tabela que contém informações de fuso horário.</span><span class="sxs-lookup"><span data-stu-id="94f97-118">The lower WORD specifies an index into a table that contains time zone information.</span></span> <span data-ttu-id="94f97-119">Partir da palavra superior, somente o bit mais alto é lido.</span><span class="sxs-lookup"><span data-stu-id="94f97-119">From the upper WORD, only the highest bit is read.</span></span> <span data-ttu-id="94f97-120">Se esse bit é definido, então o fuso horário referenciado não observará será seguido horário de verão (DST), caso contrário as datas do horário de verão detalhadas nos [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="94f97-120">If that bit is set, then the time zone referenced will not observe daylight saving time (DST), otherwise the DST dates detailed in [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) will be followed.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="94f97-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="94f97-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="94f97-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="94f97-122">Protocol specifications</span></span>

<span data-ttu-id="94f97-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94f97-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94f97-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="94f97-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="94f97-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="94f97-125">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="94f97-126">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="94f97-126">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="94f97-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94f97-127">Header files</span></span>

<span data-ttu-id="94f97-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="94f97-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="94f97-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="94f97-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="94f97-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="94f97-130">See also</span></span>



[<span data-ttu-id="94f97-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="94f97-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="94f97-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="94f97-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="94f97-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="94f97-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="94f97-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="94f97-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


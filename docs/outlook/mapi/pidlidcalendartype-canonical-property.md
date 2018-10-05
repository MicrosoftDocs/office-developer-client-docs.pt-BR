---
title: Propriedade canônica PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396516"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="55318-103">Propriedade canônica PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="55318-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="55318-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55318-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55318-105">Especifica o valor do campo CalendarType da propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="55318-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55318-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="55318-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55318-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="55318-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="55318-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="55318-108">Property set:</span></span>  <br/> |<span data-ttu-id="55318-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="55318-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="55318-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="55318-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55318-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="55318-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="55318-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="55318-112">Data type:</span></span>  <br/> |<span data-ttu-id="55318-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55318-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55318-114">Área:</span><span class="sxs-lookup"><span data-stu-id="55318-114">Area:</span></span>  <br/> |<span data-ttu-id="55318-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="55318-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55318-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="55318-116">Remarks</span></span>

<span data-ttu-id="55318-117">Quando a solicitação de reunião representa uma série recorrente ou uma exceção, esse é o valor do campo CalendarType da propriedade **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="55318-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="55318-118">Caso contrário, essa propriedade não for definida e considerada 0.</span><span class="sxs-lookup"><span data-stu-id="55318-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="55318-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55318-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55318-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="55318-120">Protocol specifications</span></span>

<span data-ttu-id="55318-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55318-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55318-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="55318-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55318-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55318-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55318-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="55318-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55318-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55318-125">Header files</span></span>

<span data-ttu-id="55318-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55318-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="55318-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="55318-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55318-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="55318-128">See also</span></span>



[<span data-ttu-id="55318-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55318-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55318-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="55318-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55318-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="55318-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55318-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="55318-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


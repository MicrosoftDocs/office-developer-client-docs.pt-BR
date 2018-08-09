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
ms.openlocfilehash: 8e3017d18491fde6b66c3173c43b8b9d0ee37ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768326"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="c6781-103">Propriedade canônica PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="c6781-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="c6781-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6781-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6781-105">Especifica o valor do campo CalendarType da propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c6781-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6781-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c6781-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6781-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="c6781-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="c6781-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="c6781-108">Property set:</span></span>  <br/> |<span data-ttu-id="c6781-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="c6781-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="c6781-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="c6781-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c6781-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="c6781-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="c6781-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c6781-112">Data type:</span></span>  <br/> |<span data-ttu-id="c6781-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c6781-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c6781-114">Área:</span><span class="sxs-lookup"><span data-stu-id="c6781-114">Area:</span></span>  <br/> |<span data-ttu-id="c6781-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="c6781-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6781-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6781-116">Remarks</span></span>

<span data-ttu-id="c6781-117">Quando a solicitação de reunião representa uma série recorrente ou uma exceção, esse é o valor do campo CalendarType da propriedade **dispidApptRecur** .</span><span class="sxs-lookup"><span data-stu-id="c6781-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="c6781-118">Caso contrário, essa propriedade não for definida e considerada 0.</span><span class="sxs-lookup"><span data-stu-id="c6781-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6781-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6781-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6781-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="c6781-120">Protocol specifications</span></span>

<span data-ttu-id="c6781-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6781-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6781-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6781-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6781-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6781-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6781-124">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="c6781-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6781-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c6781-125">Header files</span></span>

<span data-ttu-id="c6781-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6781-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6781-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c6781-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6781-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6781-128">See also</span></span>



[<span data-ttu-id="c6781-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c6781-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6781-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c6781-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6781-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c6781-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6781-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c6781-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395403"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="d09e7-103">Propriedade canônica PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="d09e7-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="d09e7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d09e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d09e7-105">Representa o período de tempo, em minutos, quando um compromisso agendado.</span><span class="sxs-lookup"><span data-stu-id="d09e7-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d09e7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d09e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d09e7-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="d09e7-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="d09e7-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="d09e7-108">Property set:</span></span>  <br/> |<span data-ttu-id="d09e7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="d09e7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="d09e7-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="d09e7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d09e7-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="d09e7-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="d09e7-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d09e7-112">Data type:</span></span>  <br/> |<span data-ttu-id="d09e7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d09e7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d09e7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d09e7-114">Area:</span></span>  <br/> |<span data-ttu-id="d09e7-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="d09e7-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d09e7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d09e7-116">Remarks</span></span>

<span data-ttu-id="d09e7-117">O valor deve ser o número de minutos entre as propriedades de **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) e o valor de **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d09e7-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d09e7-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d09e7-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d09e7-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d09e7-119">Protocol specifications</span></span>

<span data-ttu-id="d09e7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d09e7-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d09e7-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d09e7-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d09e7-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d09e7-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d09e7-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="d09e7-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d09e7-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d09e7-124">Header files</span></span>

<span data-ttu-id="d09e7-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d09e7-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d09e7-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d09e7-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d09e7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d09e7-127">See also</span></span>



[<span data-ttu-id="d09e7-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d09e7-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d09e7-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d09e7-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d09e7-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d09e7-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d09e7-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d09e7-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


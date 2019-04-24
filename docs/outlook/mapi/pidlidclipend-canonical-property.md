---
title: Propriedade canônica PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 71a0a50f26b26d65ed34f38c2a0c7f930e6082a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349179"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="dc582-103">Propriedade canônica PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="dc582-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="dc582-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc582-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc582-105">Especifica a data e a hora de término do evento em tempo universal coordenado (UTC) para objetos de calendário de instância única.</span><span class="sxs-lookup"><span data-stu-id="dc582-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc582-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dc582-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dc582-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="dc582-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="dc582-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="dc582-108">Property set:</span></span>  <br/> |<span data-ttu-id="dc582-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="dc582-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="dc582-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="dc582-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="dc582-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="dc582-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="dc582-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dc582-112">Data type:</span></span>  <br/> |<span data-ttu-id="dc582-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="dc582-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="dc582-114">Área:</span><span class="sxs-lookup"><span data-stu-id="dc582-114">Area:</span></span>  <br/> |<span data-ttu-id="dc582-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="dc582-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc582-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc582-116">Remarks</span></span>

<span data-ttu-id="dc582-117">Para objetos de calendário de instância única, ele especifica a data e a hora de término do evento em UTC.</span><span class="sxs-lookup"><span data-stu-id="dc582-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="dc582-118">Para uma série recorrente, essa propriedade especifica a meia-noite na data da última instância da série recorrente em UTC, a menos que a série recorrente tenha nenhuma extremidade, caso em que o valor deve ser de 31 de agosto de 4500, 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="dc582-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="dc582-119">O valor dessa propriedade deve ser definido como o valor de **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dc582-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="dc582-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc582-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dc582-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="dc582-121">Protocol specifications</span></span>

<span data-ttu-id="dc582-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc582-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc582-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dc582-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dc582-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc582-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dc582-125">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="dc582-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dc582-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc582-126">Header files</span></span>

<span data-ttu-id="dc582-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dc582-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="dc582-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dc582-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dc582-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc582-129">See also</span></span>



[<span data-ttu-id="dc582-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dc582-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dc582-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dc582-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dc582-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dc582-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dc582-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dc582-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


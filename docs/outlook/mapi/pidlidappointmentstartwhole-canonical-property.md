---
title: Propriedade canônica PidLidAppointmentStartWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStartWhole
api_type:
- COM
ms.assetid: e5e8ed98-57af-40d0-85c4-9d9832626e6b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6f9fb9c3f02e66fd01e89742edcfba7391c36e3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345371"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="735e8-103">Propriedade canônica PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="735e8-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="735e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="735e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="735e8-105">Representa a data e a hora em que um compromisso começa.</span><span class="sxs-lookup"><span data-stu-id="735e8-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="735e8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="735e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="735e8-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="735e8-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="735e8-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="735e8-108">Property set:</span></span>  <br/> |<span data-ttu-id="735e8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="735e8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="735e8-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="735e8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="735e8-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="735e8-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="735e8-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="735e8-112">Data type:</span></span>  <br/> |<span data-ttu-id="735e8-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="735e8-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="735e8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="735e8-114">Area:</span></span>  <br/> |<span data-ttu-id="735e8-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="735e8-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="735e8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="735e8-116">Remarks</span></span>

<span data-ttu-id="735e8-117">Essa propriedade especifica a data e a hora de início do evento.</span><span class="sxs-lookup"><span data-stu-id="735e8-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="735e8-118">Essa propriedade deve estar no Tempo Universal Coordenado (UTC) e deve ser menor do que o valor da propriedade **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="735e8-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="735e8-119">Para uma série recorrente, essa propriedade é a data e a hora de início da primeira instância de acordo com o padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="735e8-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="735e8-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="735e8-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="735e8-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="735e8-121">Protocol specifications</span></span>

<span data-ttu-id="735e8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="735e8-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="735e8-123">Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="735e8-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="735e8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="735e8-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="735e8-125">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="735e8-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="735e8-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="735e8-126">Header files</span></span>

<span data-ttu-id="735e8-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="735e8-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="735e8-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="735e8-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="735e8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="735e8-129">See also</span></span>



[<span data-ttu-id="735e8-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="735e8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="735e8-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="735e8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="735e8-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="735e8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="735e8-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="735e8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


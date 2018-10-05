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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389131"
---
# <a name="pidlidappointmentstartwhole-canonical-property"></a><span data-ttu-id="5c92d-103">Propriedade canônica PidLidAppointmentStartWhole</span><span class="sxs-lookup"><span data-stu-id="5c92d-103">PidLidAppointmentStartWhole Canonical Property</span></span>

  
  
<span data-ttu-id="5c92d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c92d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c92d-105">Representa a data e hora de início de um compromisso.</span><span class="sxs-lookup"><span data-stu-id="5c92d-105">Represents the date and time when an appointment begins.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c92d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5c92d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c92d-107">dispidApptStartWhole</span><span class="sxs-lookup"><span data-stu-id="5c92d-107">dispidApptStartWhole</span></span>  <br/> |
|<span data-ttu-id="5c92d-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5c92d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5c92d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5c92d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5c92d-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5c92d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5c92d-111">0x0000820D</span><span class="sxs-lookup"><span data-stu-id="5c92d-111">0x0000820D</span></span>  <br/> |
|<span data-ttu-id="5c92d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5c92d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5c92d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="5c92d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="5c92d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5c92d-114">Area:</span></span>  <br/> |<span data-ttu-id="5c92d-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="5c92d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c92d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c92d-116">Remarks</span></span>

<span data-ttu-id="5c92d-117">Essa propriedade especifica a data de início e a hora do evento.</span><span class="sxs-lookup"><span data-stu-id="5c92d-117">This property specifies the start date and time of the event.</span></span> <span data-ttu-id="5c92d-118">Esta propriedade deve ser no tempo Universal Coordenado (UTC) e deve ser menor do que o valor da propriedade **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5c92d-118">This property must be in Coordinated Universal Time (UTC) and must be less than the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) property.</span></span> <span data-ttu-id="5c92d-119">Para uma série recorrente, essa propriedade é a data de início e a hora da instância do primeira de acordo com o padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="5c92d-119">For a recurring series, this property is the start date and time of the first instance according to the recurrence pattern.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c92d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c92d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5c92d-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5c92d-121">Protocol specifications</span></span>

<span data-ttu-id="5c92d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c92d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c92d-123">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5c92d-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5c92d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5c92d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5c92d-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5c92d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5c92d-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c92d-126">Header files</span></span>

<span data-ttu-id="5c92d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c92d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c92d-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5c92d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c92d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c92d-129">See also</span></span>



[<span data-ttu-id="5c92d-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5c92d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c92d-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5c92d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c92d-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5c92d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c92d-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5c92d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


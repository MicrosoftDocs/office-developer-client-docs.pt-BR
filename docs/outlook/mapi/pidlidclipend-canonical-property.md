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
ms.openlocfilehash: 1353289da2b428fb58adecc6f7830a2eea4b519a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768340"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="1eb4d-103">Propriedade canônica PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="1eb4d-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="1eb4d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1eb4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1eb4d-105">Especifica a data de término e a hora do evento em tempo Universal Coordenado (UTC) para objetos de calendário de única instância.</span><span class="sxs-lookup"><span data-stu-id="1eb4d-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1eb4d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1eb4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1eb4d-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="1eb4d-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="1eb4d-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="1eb4d-108">Property set:</span></span>  <br/> |<span data-ttu-id="1eb4d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1eb4d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1eb4d-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="1eb4d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1eb4d-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="1eb4d-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="1eb4d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1eb4d-112">Data type:</span></span>  <br/> |<span data-ttu-id="1eb4d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1eb4d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1eb4d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1eb4d-114">Area:</span></span>  <br/> |<span data-ttu-id="1eb4d-115">Calendário</span><span class="sxs-lookup"><span data-stu-id="1eb4d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1eb4d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1eb4d-116">Remarks</span></span>

<span data-ttu-id="1eb4d-117">Para objetos de calendário de única instância, ela especifica a data de término e a hora do evento em UTC.</span><span class="sxs-lookup"><span data-stu-id="1eb4d-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="1eb4d-118">Para uma série recorrente, esta propriedade especifica meia-noite da data da última instância da série recorrente em UTC, a menos que a série recorrente não tem fim, nesse caso, o valor deve ser 31 de agosto 4500, 11:59 PM</span><span class="sxs-lookup"><span data-stu-id="1eb4d-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="1eb4d-119">O valor dessa propriedade deve ser definido como o valor de **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1eb4d-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1eb4d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1eb4d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1eb4d-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1eb4d-121">Protocol specifications</span></span>

<span data-ttu-id="1eb4d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb4d-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb4d-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1eb4d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1eb4d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1eb4d-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1eb4d-125">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="1eb4d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1eb4d-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1eb4d-126">Header files</span></span>

<span data-ttu-id="1eb4d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1eb4d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1eb4d-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1eb4d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1eb4d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1eb4d-129">See also</span></span>



[<span data-ttu-id="1eb4d-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb4d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1eb4d-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1eb4d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1eb4d-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1eb4d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1eb4d-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1eb4d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


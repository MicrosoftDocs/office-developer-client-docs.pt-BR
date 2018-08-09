---
title: Propriedade canônica PidLidAppointmentReplyTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentReplyTime
api_type:
- COM
ms.assetid: 80a2608b-fc44-455a-86be-d6235caba99e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bc2af5205e6e07b56212a6cf7077f9ef4bee89c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768309"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="04203-103">Propriedade canônica PidLidAppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="04203-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="04203-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04203-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04203-105">Especifica a data e hora de quando o participante respondeu a solicitação de reunião um recebida ou atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="04203-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="04203-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="04203-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="04203-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="04203-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="04203-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="04203-108">Property set:</span></span>  <br/> |<span data-ttu-id="04203-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="04203-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="04203-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="04203-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="04203-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="04203-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="04203-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="04203-112">Data type:</span></span>  <br/> |<span data-ttu-id="04203-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="04203-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="04203-114">Área:</span><span class="sxs-lookup"><span data-stu-id="04203-114">Area:</span></span>  <br/> |<span data-ttu-id="04203-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="04203-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04203-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="04203-116">Remarks</span></span>

<span data-ttu-id="04203-117">O valor deve ser especificado no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="04203-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="04203-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="04203-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="04203-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="04203-119">Protocol specifications</span></span>

<span data-ttu-id="04203-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04203-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04203-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="04203-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="04203-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="04203-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="04203-123">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="04203-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="04203-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="04203-124">Header files</span></span>

<span data-ttu-id="04203-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="04203-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="04203-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="04203-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="04203-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="04203-127">See also</span></span>



[<span data-ttu-id="04203-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="04203-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="04203-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="04203-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="04203-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="04203-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="04203-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="04203-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


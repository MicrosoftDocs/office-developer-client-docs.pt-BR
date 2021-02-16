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
ms.openlocfilehash: ba79498569c544d1b0ee22e968477d5b68812c09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331784"
---
# <a name="pidlidappointmentreplytime-canonical-property"></a><span data-ttu-id="418fb-103">Propriedade canônica PidLidAppointmentReplyTime</span><span class="sxs-lookup"><span data-stu-id="418fb-103">PidLidAppointmentReplyTime Canonical Property</span></span>

  
  
<span data-ttu-id="418fb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="418fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="418fb-105">Especifica a data e a hora em que o participante respondeu a uma solicitação de reunião recebida ou atualização da reunião.</span><span class="sxs-lookup"><span data-stu-id="418fb-105">Specifies the date and time when the attendee responded to a received meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="418fb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="418fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="418fb-107">dispidApptReplyTime</span><span class="sxs-lookup"><span data-stu-id="418fb-107">dispidApptReplyTime</span></span>  <br/> |
|<span data-ttu-id="418fb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="418fb-108">Property set:</span></span>  <br/> |<span data-ttu-id="418fb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="418fb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="418fb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="418fb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="418fb-111">0x00008220</span><span class="sxs-lookup"><span data-stu-id="418fb-111">0x00008220</span></span>  <br/> |
|<span data-ttu-id="418fb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="418fb-112">Data type:</span></span>  <br/> |<span data-ttu-id="418fb-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="418fb-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="418fb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="418fb-114">Area:</span></span>  <br/> |<span data-ttu-id="418fb-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="418fb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="418fb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="418fb-116">Remarks</span></span>

<span data-ttu-id="418fb-117">O valor deve ser especificado em UTC (Tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="418fb-117">The value must be specified in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="418fb-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="418fb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="418fb-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="418fb-119">Protocol specifications</span></span>

<span data-ttu-id="418fb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="418fb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="418fb-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="418fb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="418fb-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="418fb-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="418fb-123">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="418fb-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="418fb-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="418fb-124">Header files</span></span>

<span data-ttu-id="418fb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="418fb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="418fb-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="418fb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="418fb-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="418fb-127">See also</span></span>



[<span data-ttu-id="418fb-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="418fb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="418fb-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="418fb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="418fb-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="418fb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="418fb-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="418fb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


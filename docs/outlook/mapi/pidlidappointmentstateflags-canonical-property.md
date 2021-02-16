---
title: Propriedade canônica PidLidAppointmentStateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentStateFlags
api_type:
- COM
ms.assetid: 1e5f0f83-c40b-4b3a-8492-61d1b53b1e3c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e365c78ea6457e7da79e3d1c749baa922a01acbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345357"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="0a7c7-103">Propriedade canônica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="0a7c7-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="0a7c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a7c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a7c7-105">Especifica um campo de bits que descreve o estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0a7c7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0a7c7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a7c7-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="0a7c7-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="0a7c7-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="0a7c7-108">Property set:</span></span>  <br/> |<span data-ttu-id="0a7c7-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0a7c7-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0a7c7-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0a7c7-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0a7c7-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="0a7c7-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="0a7c7-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0a7c7-112">Data type:</span></span>  <br/> |<span data-ttu-id="0a7c7-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0a7c7-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0a7c7-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0a7c7-114">Area:</span></span>  <br/> |<span data-ttu-id="0a7c7-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="0a7c7-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a7c7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a7c7-116">Remarks</span></span>

<span data-ttu-id="0a7c7-117">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-117">This property is not required.</span></span> <span data-ttu-id="0a7c7-118">Abaixo estão os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="0a7c7-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="0a7c7-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="0a7c7-120">Esse sinalizador indica que o objeto é um objeto de reunião ou um objeto relacionado à reunião.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="0a7c7-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="0a7c7-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="0a7c7-122">Esse sinalizador indica que o objeto representado foi recebido de outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="0a7c7-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="0a7c7-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="0a7c7-124">Esse sinalizador indica que o objeto de reunião representado pelo objeto foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="0a7c7-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a7c7-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0a7c7-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0a7c7-126">Protocol specifications</span></span>

<span data-ttu-id="0a7c7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a7c7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a7c7-128">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0a7c7-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0a7c7-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0a7c7-130">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0a7c7-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0a7c7-131">Header files</span></span>

<span data-ttu-id="0a7c7-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a7c7-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a7c7-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0a7c7-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a7c7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a7c7-134">See also</span></span>



[<span data-ttu-id="0a7c7-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7c7-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a7c7-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7c7-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a7c7-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0a7c7-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a7c7-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0a7c7-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


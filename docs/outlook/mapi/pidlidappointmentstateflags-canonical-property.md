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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391329"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="70789-103">Propriedade canônica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="70789-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="70789-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70789-105">Especifica um campo de bit que descreve o estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="70789-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70789-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="70789-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70789-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="70789-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="70789-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="70789-108">Property set:</span></span>  <br/> |<span data-ttu-id="70789-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="70789-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="70789-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="70789-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="70789-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="70789-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="70789-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="70789-112">Data type:</span></span>  <br/> |<span data-ttu-id="70789-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="70789-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="70789-114">Área:</span><span class="sxs-lookup"><span data-stu-id="70789-114">Area:</span></span>  <br/> |<span data-ttu-id="70789-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="70789-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70789-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="70789-116">Remarks</span></span>

<span data-ttu-id="70789-117">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="70789-117">This property is not required.</span></span> <span data-ttu-id="70789-118">Abaixo estão os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="70789-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="70789-119">M (asfMeeting 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="70789-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="70789-120">Esse sinalizador indica que o objeto é um objeto de reunião ou um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="70789-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="70789-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="70789-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="70789-122">Esse sinalizador indica que o objeto representado foi recebido de alguém.</span><span class="sxs-lookup"><span data-stu-id="70789-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="70789-123">C (asfCanceled 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="70789-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="70789-124">Esse sinalizador indica que o objeto de reunião representado pelo objeto foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="70789-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="70789-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="70789-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70789-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="70789-126">Protocol specifications</span></span>

<span data-ttu-id="70789-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70789-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70789-128">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="70789-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70789-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70789-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70789-130">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="70789-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70789-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="70789-131">Header files</span></span>

<span data-ttu-id="70789-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="70789-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="70789-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="70789-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70789-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="70789-134">See also</span></span>



[<span data-ttu-id="70789-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="70789-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70789-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="70789-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70789-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="70789-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70789-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="70789-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


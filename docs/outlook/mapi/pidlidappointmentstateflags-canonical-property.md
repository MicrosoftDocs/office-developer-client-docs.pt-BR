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
ms.openlocfilehash: 293eb489a1e926f0e60e823a536dacf6f409e353
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768297"
---
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="5f42a-103">Propriedade canônica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="5f42a-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5f42a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f42a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f42a-105">Especifica um campo de bit que descreve o estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="5f42a-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f42a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5f42a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f42a-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="5f42a-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="5f42a-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5f42a-108">Property set:</span></span>  <br/> |<span data-ttu-id="5f42a-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="5f42a-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="5f42a-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5f42a-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5f42a-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="5f42a-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="5f42a-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5f42a-112">Data type:</span></span>  <br/> |<span data-ttu-id="5f42a-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f42a-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f42a-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5f42a-114">Area:</span></span>  <br/> |<span data-ttu-id="5f42a-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="5f42a-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f42a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f42a-116">Remarks</span></span>

<span data-ttu-id="5f42a-117">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="5f42a-117">This property is not required.</span></span> <span data-ttu-id="5f42a-118">Abaixo estão os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5f42a-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="5f42a-119">M (asfMeeting 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="5f42a-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="5f42a-120">Esse sinalizador indica que o objeto é um objeto de reunião ou um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="5f42a-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="5f42a-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="5f42a-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="5f42a-122">Esse sinalizador indica que o objeto representado foi recebido de alguém.</span><span class="sxs-lookup"><span data-stu-id="5f42a-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="5f42a-123">C (asfCanceled 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="5f42a-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="5f42a-124">Esse sinalizador indica que o objeto de reunião representado pelo objeto foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="5f42a-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5f42a-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f42a-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f42a-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f42a-126">Protocol specifications</span></span>

<span data-ttu-id="5f42a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f42a-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f42a-128">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f42a-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f42a-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f42a-129">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f42a-130">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="5f42a-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f42a-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5f42a-131">Header files</span></span>

<span data-ttu-id="5f42a-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f42a-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f42a-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5f42a-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f42a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f42a-134">See also</span></span>



[<span data-ttu-id="5f42a-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f42a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f42a-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5f42a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f42a-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5f42a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f42a-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5f42a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


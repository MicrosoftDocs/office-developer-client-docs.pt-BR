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
# <a name="pidlidappointmentstateflags-canonical-property"></a><span data-ttu-id="1bcbd-103">Propriedade canônica PidLidAppointmentStateFlags</span><span class="sxs-lookup"><span data-stu-id="1bcbd-103">PidLidAppointmentStateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1bcbd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1bcbd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1bcbd-105">Especifica um campo de bits que descreve o estado do objeto.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-105">Specifies a bit field that describes the state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1bcbd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1bcbd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1bcbd-107">dispidApptStateFlags</span><span class="sxs-lookup"><span data-stu-id="1bcbd-107">dispidApptStateFlags</span></span>  <br/> |
|<span data-ttu-id="1bcbd-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="1bcbd-108">Property set:</span></span>  <br/> |<span data-ttu-id="1bcbd-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1bcbd-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1bcbd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1bcbd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1bcbd-111">0x00008217</span><span class="sxs-lookup"><span data-stu-id="1bcbd-111">0x00008217</span></span>  <br/> |
|<span data-ttu-id="1bcbd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1bcbd-112">Data type:</span></span>  <br/> |<span data-ttu-id="1bcbd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1bcbd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1bcbd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1bcbd-114">Area:</span></span>  <br/> |<span data-ttu-id="1bcbd-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="1bcbd-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bcbd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bcbd-116">Remarks</span></span>

<span data-ttu-id="1bcbd-117">Esta propriedade não é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-117">This property is not required.</span></span> <span data-ttu-id="1bcbd-118">Veja a seguir os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="1bcbd-119">M (asfMeeting, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1bcbd-119">M (asfMeeting, 0x00000001)</span></span>
  
> <span data-ttu-id="1bcbd-120">Este sinalizador indica que o objeto é um objeto de reunião ou um objeto relacionado à reunião.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-120">This flag indicates that the object is a meeting object or a meeting-related object.</span></span>
    
<span data-ttu-id="1bcbd-121">R (asfReceived, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1bcbd-121">R (asfReceived, 0x00000002)</span></span>
  
> <span data-ttu-id="1bcbd-122">Este sinalizador indica que o objeto representado foi recebido de outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-122">This flag indicates that the represented object was received from someone else.</span></span>
    
<span data-ttu-id="1bcbd-123">C (asfCanceled, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="1bcbd-123">C (asfCanceled, 0x00000004)</span></span>
  
> <span data-ttu-id="1bcbd-124">Este sinalizador indica que o objeto de reunião representado pelo objeto foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-124">This flag indicates that the meeting object represented by the object has been canceled.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1bcbd-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bcbd-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1bcbd-126">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="1bcbd-126">Protocol specifications</span></span>

<span data-ttu-id="1bcbd-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bcbd-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bcbd-128">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1bcbd-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1bcbd-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1bcbd-130">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1bcbd-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1bcbd-131">Header files</span></span>

<span data-ttu-id="1bcbd-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1bcbd-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="1bcbd-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1bcbd-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bcbd-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bcbd-134">See also</span></span>



[<span data-ttu-id="1bcbd-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1bcbd-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1bcbd-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1bcbd-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1bcbd-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1bcbd-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1bcbd-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1bcbd-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


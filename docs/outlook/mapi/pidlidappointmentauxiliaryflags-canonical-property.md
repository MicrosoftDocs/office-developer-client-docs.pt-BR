---
title: Propriedade canônica PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396831"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="54511-103">Propriedade canônica PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="54511-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="54511-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54511-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54511-105">Especifica um campo de bit que descreve o estado auxiliar do objeto.</span><span class="sxs-lookup"><span data-stu-id="54511-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54511-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="54511-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54511-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="54511-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="54511-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="54511-108">Property set:</span></span>  <br/> |<span data-ttu-id="54511-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="54511-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="54511-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="54511-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="54511-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="54511-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="54511-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="54511-112">Data type:</span></span>  <br/> |<span data-ttu-id="54511-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="54511-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="54511-114">Área:</span><span class="sxs-lookup"><span data-stu-id="54511-114">Area:</span></span>  <br/> |<span data-ttu-id="54511-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="54511-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54511-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="54511-116">Remarks</span></span>

<span data-ttu-id="54511-117">Essa propriedade não é necessária.</span><span class="sxs-lookup"><span data-stu-id="54511-117">This property is not required.</span></span> <span data-ttu-id="54511-118">Abaixo estão os sinalizadores individuais que podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="54511-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="54511-119">C (auxApptFlagCopied 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="54511-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="54511-120">Esse sinalizador indica que o objeto calendar foi copiado de outra pasta de calendário.</span><span class="sxs-lookup"><span data-stu-id="54511-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="54511-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="54511-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="54511-122">Esse sinalizador em uma solicitação de reunião indica que o cliente ou servidor deve enviar uma resposta de reunião ao organizador quando uma resposta é escolhida.</span><span class="sxs-lookup"><span data-stu-id="54511-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="54511-123">F (auxApptFlagForwarded 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="54511-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="54511-124">Esse sinalizador em uma solicitação de reunião indica que ele foi encaminhado (incluindo sejam encaminhadas pelo organizador), em vez de ser um convite do organizador.</span><span class="sxs-lookup"><span data-stu-id="54511-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="54511-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="54511-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54511-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="54511-126">Protocol specifications</span></span>

<span data-ttu-id="54511-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54511-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54511-128">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="54511-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54511-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54511-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54511-130">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="54511-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54511-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54511-131">Header files</span></span>

<span data-ttu-id="54511-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54511-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="54511-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="54511-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54511-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="54511-134">See also</span></span>



[<span data-ttu-id="54511-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="54511-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54511-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="54511-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54511-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="54511-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54511-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="54511-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


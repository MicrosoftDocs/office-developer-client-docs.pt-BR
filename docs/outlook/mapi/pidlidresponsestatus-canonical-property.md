---
title: Propriedade canônica PidLidResponseStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidResponseStatus
api_type:
- COM
ms.assetid: e56142fd-204b-497e-83b9-59f9acda6cb4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e6aa8407459fef5fd9657e9d2887f0ae78ff9c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585462"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="b5c26-103">Propriedade canônica PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="b5c26-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b5c26-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5c26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5c26-105">Especifica o status de resposta de um participante.</span><span class="sxs-lookup"><span data-stu-id="b5c26-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5c26-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b5c26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5c26-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="b5c26-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="b5c26-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="b5c26-108">Property set:</span></span>  <br/> |<span data-ttu-id="b5c26-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b5c26-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b5c26-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="b5c26-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b5c26-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="b5c26-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="b5c26-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b5c26-112">Data type:</span></span>  <br/> |<span data-ttu-id="b5c26-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5c26-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5c26-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b5c26-114">Area:</span></span>  <br/> |<span data-ttu-id="b5c26-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="b5c26-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5c26-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5c26-116">Remarks</span></span>

<span data-ttu-id="b5c26-117">O status de resposta deve ser um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5c26-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="b5c26-118">**Status de resposta**</span><span class="sxs-lookup"><span data-stu-id="b5c26-118">**Response status**</span></span>|<span data-ttu-id="b5c26-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b5c26-119">**Value**</span></span>|<span data-ttu-id="b5c26-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5c26-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b5c26-121">respNone</span><span class="sxs-lookup"><span data-stu-id="b5c26-121">respNone</span></span>  <br/> |<span data-ttu-id="b5c26-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5c26-122">0x00000000</span></span>  <br/> |<span data-ttu-id="b5c26-123">Nenhuma resposta é necessária para este objeto.</span><span class="sxs-lookup"><span data-stu-id="b5c26-123">No response is required for this object.</span></span> <span data-ttu-id="b5c26-124">Esse é o caso de objetos de compromisso e objetos de resposta de reunião.</span><span class="sxs-lookup"><span data-stu-id="b5c26-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="b5c26-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="b5c26-125">respOrganized</span></span>  <br/> |<span data-ttu-id="b5c26-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b5c26-126">0x00000001</span></span>  <br/> |<span data-ttu-id="b5c26-127">Esta reunião pertence ao Media Gallery.</span><span class="sxs-lookup"><span data-stu-id="b5c26-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="b5c26-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="b5c26-128">respTentative</span></span>  <br/> |<span data-ttu-id="b5c26-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b5c26-129">0x00000002</span></span>  <br/> |<span data-ttu-id="b5c26-130">Esse valor na reunião do participante indica que o participante aceitou provisoriamente a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="b5c26-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="b5c26-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="b5c26-131">respAccepted</span></span>  <br/> |<span data-ttu-id="b5c26-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b5c26-132">0x00000003</span></span>  <br/> |<span data-ttu-id="b5c26-133">Esse valor em t de reunião do participante indica que o participante aceitou a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="b5c26-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="b5c26-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="b5c26-134">respDeclined</span></span>  <br/> |<span data-ttu-id="b5c26-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b5c26-135">0x00000004</span></span>  <br/> |<span data-ttu-id="b5c26-136">Esse valor na reunião do participante indica que o participante recusou a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="b5c26-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="b5c26-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="b5c26-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="b5c26-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b5c26-138">0x00000005</span></span>  <br/> |<span data-ttu-id="b5c26-139">Esse valor na reunião do participante indica que o nome do participante ainda não tiver respondido.</span><span class="sxs-lookup"><span data-stu-id="b5c26-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="b5c26-140">Esse valor é na solicitação de reunião, atualização de reunião e cancelamento de reunião.</span><span class="sxs-lookup"><span data-stu-id="b5c26-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b5c26-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5c26-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5c26-142">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b5c26-142">Protocol specifications</span></span>

<span data-ttu-id="b5c26-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5c26-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5c26-144">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5c26-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5c26-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5c26-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5c26-146">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="b5c26-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5c26-147">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5c26-147">Header files</span></span>

<span data-ttu-id="b5c26-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5c26-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5c26-149">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5c26-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5c26-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5c26-150">See also</span></span>



[<span data-ttu-id="b5c26-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5c26-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5c26-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b5c26-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5c26-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b5c26-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5c26-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b5c26-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


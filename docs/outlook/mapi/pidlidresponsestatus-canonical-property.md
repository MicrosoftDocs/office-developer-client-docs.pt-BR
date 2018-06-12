---
title: Propriedade canônico de PidLidResponseStatus
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0bfa3a01613c49b122e92e4ac281e5b20b5f07ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768631"
---
# <a name="pidlidresponsestatus-canonical-property"></a><span data-ttu-id="830fb-103">Propriedade canônico de PidLidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="830fb-103">PidLidResponseStatus Canonical Property</span></span>

  
  
<span data-ttu-id="830fb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="830fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="830fb-105">Especifica o status de resposta de um participante.</span><span class="sxs-lookup"><span data-stu-id="830fb-105">Specifies the response status of an attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="830fb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="830fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="830fb-107">dispidResponseStatus</span><span class="sxs-lookup"><span data-stu-id="830fb-107">dispidResponseStatus</span></span>  <br/> |
|<span data-ttu-id="830fb-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="830fb-108">Property set:</span></span>  <br/> |<span data-ttu-id="830fb-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="830fb-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="830fb-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="830fb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="830fb-111">0x00008218</span><span class="sxs-lookup"><span data-stu-id="830fb-111">0x00008218</span></span>  <br/> |
|<span data-ttu-id="830fb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="830fb-112">Data type:</span></span>  <br/> |<span data-ttu-id="830fb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="830fb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="830fb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="830fb-114">Area:</span></span>  <br/> |<span data-ttu-id="830fb-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="830fb-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="830fb-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="830fb-116">Remarks</span></span>

<span data-ttu-id="830fb-117">O status de resposta deve ser um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="830fb-117">The response status must be one of the values in the table below.</span></span>
  
|<span data-ttu-id="830fb-118">**Status de resposta**</span><span class="sxs-lookup"><span data-stu-id="830fb-118">**Response status**</span></span>|<span data-ttu-id="830fb-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="830fb-119">**Value**</span></span>|<span data-ttu-id="830fb-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="830fb-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="830fb-121">respNone</span><span class="sxs-lookup"><span data-stu-id="830fb-121">respNone</span></span>  <br/> |<span data-ttu-id="830fb-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="830fb-122">0x00000000</span></span>  <br/> |<span data-ttu-id="830fb-123">Nenhuma resposta é necessária para este objeto.</span><span class="sxs-lookup"><span data-stu-id="830fb-123">No response is required for this object.</span></span> <span data-ttu-id="830fb-124">Esse é o caso de objetos de compromisso e objetos de resposta de reunião.</span><span class="sxs-lookup"><span data-stu-id="830fb-124">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="830fb-125">respOrganized</span><span class="sxs-lookup"><span data-stu-id="830fb-125">respOrganized</span></span>  <br/> |<span data-ttu-id="830fb-126">0x00000001</span><span class="sxs-lookup"><span data-stu-id="830fb-126">0x00000001</span></span>  <br/> |<span data-ttu-id="830fb-127">Esta reunião pertence ao Media Gallery.</span><span class="sxs-lookup"><span data-stu-id="830fb-127">This meeting belongs to the organizer.</span></span>  <br/> |
|<span data-ttu-id="830fb-128">respTentative</span><span class="sxs-lookup"><span data-stu-id="830fb-128">respTentative</span></span>  <br/> |<span data-ttu-id="830fb-129">0x00000002</span><span class="sxs-lookup"><span data-stu-id="830fb-129">0x00000002</span></span>  <br/> |<span data-ttu-id="830fb-130">Esse valor na reunião do participante indica que o participante aceitou provisoriamente a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="830fb-130">This value on the attendee's meeting indicates that the attendee has tentatively accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="830fb-131">respAccepted</span><span class="sxs-lookup"><span data-stu-id="830fb-131">respAccepted</span></span>  <br/> |<span data-ttu-id="830fb-132">0x00000003</span><span class="sxs-lookup"><span data-stu-id="830fb-132">0x00000003</span></span>  <br/> |<span data-ttu-id="830fb-133">Esse valor em t de reunião do participante indica que o participante aceitou a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="830fb-133">This value on the attendee's meeting t indicates that the attendee has accepted the meeting request.</span></span>  <br/> |
|<span data-ttu-id="830fb-134">respDeclined</span><span class="sxs-lookup"><span data-stu-id="830fb-134">respDeclined</span></span>  <br/> |<span data-ttu-id="830fb-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="830fb-135">0x00000004</span></span>  <br/> |<span data-ttu-id="830fb-136">Esse valor na reunião do participante indica que o participante recusou a solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="830fb-136">This value on the attendee's meeting indicates that the attendee has declined the meeting request.</span></span>  <br/> |
|<span data-ttu-id="830fb-137">respNotResponded</span><span class="sxs-lookup"><span data-stu-id="830fb-137">respNotResponded</span></span>  <br/> |<span data-ttu-id="830fb-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="830fb-138">0x00000005</span></span>  <br/> |<span data-ttu-id="830fb-139">Esse valor na reunião do participante indica que o nome do participante ainda não tiver respondido.</span><span class="sxs-lookup"><span data-stu-id="830fb-139">This value on the attendee's meeting indicates the attendee has not yet responded.</span></span> <span data-ttu-id="830fb-140">Esse valor é na solicitação de reunião, atualização de reunião e cancelamento de reunião.</span><span class="sxs-lookup"><span data-stu-id="830fb-140">This value is on the meeting request, meeting update, and meeting cancelation.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="830fb-141">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="830fb-141">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="830fb-142">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="830fb-142">Protocol specifications</span></span>

<span data-ttu-id="830fb-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="830fb-143">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="830fb-144">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="830fb-144">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="830fb-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="830fb-145">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="830fb-146">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="830fb-146">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="830fb-147">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="830fb-147">Header files</span></span>

<span data-ttu-id="830fb-148">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="830fb-148">Mapidefs.h</span></span>
  
> <span data-ttu-id="830fb-149">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="830fb-149">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="830fb-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="830fb-150">See also</span></span>



[<span data-ttu-id="830fb-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="830fb-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="830fb-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="830fb-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="830fb-153">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="830fb-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="830fb-154">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="830fb-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


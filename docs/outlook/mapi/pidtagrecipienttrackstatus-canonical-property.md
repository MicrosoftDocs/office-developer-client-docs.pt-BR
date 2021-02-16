---
title: Propriedade canônica PidTagRecipientTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355283"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a><span data-ttu-id="44554-103">Propriedade canônica PidTagRecipientTrackStatus</span><span class="sxs-lookup"><span data-stu-id="44554-103">PidTagRecipientTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="44554-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44554-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44554-105">Indica o status de resposta retornado pelo participante.</span><span class="sxs-lookup"><span data-stu-id="44554-105">Indicates the response status returned by the attendee.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="44554-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="44554-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="44554-107">PR_RECIPIENT_TRACKSTATUS</span><span class="sxs-lookup"><span data-stu-id="44554-107">PR_RECIPIENT_TRACKSTATUS</span></span>  <br/> |
|<span data-ttu-id="44554-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="44554-108">Identifier:</span></span>  <br/> |<span data-ttu-id="44554-109">0x5FFF</span><span class="sxs-lookup"><span data-stu-id="44554-109">0x5FFF</span></span>  <br/> |
|<span data-ttu-id="44554-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="44554-110">Data type:</span></span>  <br/> |<span data-ttu-id="44554-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="44554-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="44554-112">Área:</span><span class="sxs-lookup"><span data-stu-id="44554-112">Area:</span></span>  <br/> |<span data-ttu-id="44554-113">Destinatário de transporte</span><span class="sxs-lookup"><span data-stu-id="44554-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44554-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="44554-114">Remarks</span></span>

<span data-ttu-id="44554-115">Se esse valor não for definido, ele deverá ser assumido como respNone.</span><span class="sxs-lookup"><span data-stu-id="44554-115">If this value is not set, it must be assumed to be respNone.</span></span> <span data-ttu-id="44554-116">Caso contrário, ele deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="44554-116">Otherwise, it must be one of the following:</span></span>
  
|<span data-ttu-id="44554-117">**Status da resposta**</span><span class="sxs-lookup"><span data-stu-id="44554-117">**Response status**</span></span>|<span data-ttu-id="44554-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="44554-118">**Value**</span></span>|<span data-ttu-id="44554-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="44554-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="44554-120">respNone</span><span class="sxs-lookup"><span data-stu-id="44554-120">respNone</span></span>  <br/> |<span data-ttu-id="44554-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44554-121">0x00000000</span></span>  <br/> |<span data-ttu-id="44554-122">Nenhuma resposta é necessária para este objeto.</span><span class="sxs-lookup"><span data-stu-id="44554-122">No response is required for this object.</span></span> <span data-ttu-id="44554-123">Esse é o caso para objetos de compromisso e objetos de resposta de reunião.</span><span class="sxs-lookup"><span data-stu-id="44554-123">This is the case for appointment objects and meeting response objects.</span></span>  <br/> |
|<span data-ttu-id="44554-124">respTentative</span><span class="sxs-lookup"><span data-stu-id="44554-124">respTentative</span></span>  <br/> |<span data-ttu-id="44554-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="44554-125">0x00000002</span></span>  <br/> |<span data-ttu-id="44554-126">Esse valor no objeto de reunião do participante indica que o participante aceitou provisadamente o objeto de solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="44554-126">This value on the attendee's meeting object indicates that the attendee has tentatively accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="44554-127">respAccepted</span><span class="sxs-lookup"><span data-stu-id="44554-127">respAccepted</span></span>  <br/> |<span data-ttu-id="44554-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="44554-128">0x00000003</span></span>  <br/> |<span data-ttu-id="44554-129">Esse valor no objeto de reunião do participante indica que o participante aceitou o objeto de solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="44554-129">This value on the attendee's meeting object indicates that the attendee has accepted the meeting request object.</span></span>  <br/> |
|<span data-ttu-id="44554-130">respDeclined</span><span class="sxs-lookup"><span data-stu-id="44554-130">respDeclined</span></span>  <br/> |<span data-ttu-id="44554-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="44554-131">0x00000004</span></span>  <br/> |<span data-ttu-id="44554-132">Esse valor no objeto de reunião do participante indica que o participante recusou o objeto de solicitação de reunião.</span><span class="sxs-lookup"><span data-stu-id="44554-132">This value on the attendee's meeting object indicates that the attendee has declined the meeting request object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="44554-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="44554-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="44554-134">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="44554-134">Protocol specifications</span></span>

<span data-ttu-id="44554-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44554-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44554-136">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="44554-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="44554-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44554-137">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44554-138">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="44554-138">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="44554-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="44554-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="44554-140">Lida com objetos de mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="44554-140">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="44554-141">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="44554-141">Header files</span></span>

<span data-ttu-id="44554-142">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="44554-142">Mapidefs.h</span></span>
  
> <span data-ttu-id="44554-143">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="44554-143">Provides data type definitions.</span></span>
    
<span data-ttu-id="44554-144">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="44554-144">Mapitags.h</span></span>
  
> <span data-ttu-id="44554-145">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="44554-145">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="44554-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="44554-146">See also</span></span>



[<span data-ttu-id="44554-147">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="44554-147">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="44554-148">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="44554-148">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="44554-149">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="44554-149">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="44554-150">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="44554-150">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


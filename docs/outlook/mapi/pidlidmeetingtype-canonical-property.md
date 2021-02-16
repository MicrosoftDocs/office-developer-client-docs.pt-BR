---
title: Propriedade canônica PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331573"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="20895-103">Propriedade canônica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="20895-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="20895-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20895-105">Indica o tipo de solicitação de reunião ou atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="20895-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20895-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="20895-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20895-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="20895-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="20895-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="20895-108">Property set:</span></span>  <br/> |<span data-ttu-id="20895-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="20895-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="20895-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="20895-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="20895-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="20895-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="20895-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="20895-112">Data type:</span></span>  <br/> |<span data-ttu-id="20895-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="20895-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="20895-114">Área:</span><span class="sxs-lookup"><span data-stu-id="20895-114">Area:</span></span>  <br/> |<span data-ttu-id="20895-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="20895-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20895-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="20895-116">Remarks</span></span>

<span data-ttu-id="20895-117">O valor dessa propriedade deve ser definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="20895-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="20895-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="20895-118">**Property**</span></span>|<span data-ttu-id="20895-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="20895-119">**Value**</span></span>|<span data-ttu-id="20895-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="20895-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="20895-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="20895-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="20895-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20895-122">0x00000000</span></span>  <br/> |<span data-ttu-id="20895-123">Não especificado.</span><span class="sxs-lookup"><span data-stu-id="20895-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="20895-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="20895-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="20895-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="20895-125">0x00000001</span></span>  <br/> |<span data-ttu-id="20895-126">Solicitação de reunião inicial.</span><span class="sxs-lookup"><span data-stu-id="20895-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="20895-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="20895-127">mtgFull</span></span>  <br/> |<span data-ttu-id="20895-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="20895-128">0x00010000</span></span>  <br/> |<span data-ttu-id="20895-129">Atualização completa.</span><span class="sxs-lookup"><span data-stu-id="20895-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="20895-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="20895-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="20895-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="20895-131">0x00020000</span></span>  <br/> |<span data-ttu-id="20895-132">Atualização informacional.</span><span class="sxs-lookup"><span data-stu-id="20895-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="20895-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="20895-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="20895-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="20895-134">0x00080000</span></span>  <br/> |<span data-ttu-id="20895-135">Uma solicitação de reunião ou atualização de reunião mais recente foi recebida após esta.</span><span class="sxs-lookup"><span data-stu-id="20895-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="20895-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="20895-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="20895-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="20895-137">0x00100000</span></span>  <br/> |<span data-ttu-id="20895-138">Isso é definido na cópia do delegante quando um representante lida com objetos relacionados à reunião.</span><span class="sxs-lookup"><span data-stu-id="20895-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="20895-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20895-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20895-140">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="20895-140">Protocol specifications</span></span>

<span data-ttu-id="20895-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20895-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20895-142">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="20895-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20895-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20895-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20895-144">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="20895-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20895-145">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="20895-145">Header files</span></span>

<span data-ttu-id="20895-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20895-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="20895-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="20895-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20895-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="20895-148">See also</span></span>



[<span data-ttu-id="20895-149">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20895-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20895-150">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="20895-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20895-151">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="20895-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20895-152">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="20895-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


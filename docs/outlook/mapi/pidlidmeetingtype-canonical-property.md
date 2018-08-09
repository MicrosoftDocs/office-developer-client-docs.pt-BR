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
ms.openlocfilehash: e61ce7798c9e41dbb707d0d5773b116f7cce02d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768531"
---
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="d1084-103">Propriedade canônica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="d1084-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="d1084-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1084-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1084-105">Indica o tipo de solicitação de reunião ou atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="d1084-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1084-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d1084-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1084-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="d1084-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="d1084-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="d1084-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1084-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="d1084-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="d1084-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="d1084-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1084-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="d1084-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="d1084-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d1084-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1084-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1084-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1084-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d1084-114">Area:</span></span>  <br/> |<span data-ttu-id="d1084-115">Reuniões</span><span class="sxs-lookup"><span data-stu-id="d1084-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1084-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1084-116">Remarks</span></span>

<span data-ttu-id="d1084-117">O valor dessa propriedade deve ser definido como um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="d1084-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="d1084-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="d1084-118">**Property**</span></span>|<span data-ttu-id="d1084-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d1084-119">**Value**</span></span>|<span data-ttu-id="d1084-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d1084-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1084-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="d1084-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="d1084-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d1084-122">0x00000000</span></span>  <br/> |<span data-ttu-id="d1084-123">Não for especificado.</span><span class="sxs-lookup"><span data-stu-id="d1084-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="d1084-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="d1084-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="d1084-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d1084-125">0x00000001</span></span>  <br/> |<span data-ttu-id="d1084-126">Solicitação de reunião inicial.</span><span class="sxs-lookup"><span data-stu-id="d1084-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="d1084-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="d1084-127">mtgFull</span></span>  <br/> |<span data-ttu-id="d1084-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d1084-128">0x00010000</span></span>  <br/> |<span data-ttu-id="d1084-129">Atualização completa.</span><span class="sxs-lookup"><span data-stu-id="d1084-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="d1084-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="d1084-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="d1084-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d1084-131">0x00020000</span></span>  <br/> |<span data-ttu-id="d1084-132">Atualização informativa.</span><span class="sxs-lookup"><span data-stu-id="d1084-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="d1084-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="d1084-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="d1084-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d1084-134">0x00080000</span></span>  <br/> |<span data-ttu-id="d1084-135">Uma solicitação de reunião mais recente ou atualização de reunião foi recebida depois deste.</span><span class="sxs-lookup"><span data-stu-id="d1084-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="d1084-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="d1084-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="d1084-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d1084-137">0x00100000</span></span>  <br/> |<span data-ttu-id="d1084-138">Isso é definido na cópia do delegator quando objetos de reuniões de alças um representante.</span><span class="sxs-lookup"><span data-stu-id="d1084-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d1084-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1084-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1084-140">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d1084-140">Protocol specifications</span></span>

<span data-ttu-id="d1084-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1084-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1084-142">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1084-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1084-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1084-143">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1084-144">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="d1084-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1084-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1084-145">Header files</span></span>

<span data-ttu-id="d1084-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1084-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1084-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d1084-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1084-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1084-148">See also</span></span>



[<span data-ttu-id="d1084-149">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d1084-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1084-150">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d1084-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1084-151">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d1084-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1084-152">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d1084-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


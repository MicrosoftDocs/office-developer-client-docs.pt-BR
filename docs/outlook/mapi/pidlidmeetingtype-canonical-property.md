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
# <a name="pidlidmeetingtype-canonical-property"></a><span data-ttu-id="23788-103">Propriedade canônica PidLidMeetingType</span><span class="sxs-lookup"><span data-stu-id="23788-103">PidLidMeetingType Canonical Property</span></span>

  
  
<span data-ttu-id="23788-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23788-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23788-105">Indica o tipo de solicitação de reunião ou atualização de reunião.</span><span class="sxs-lookup"><span data-stu-id="23788-105">Indicates the type of meeting request or meeting update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23788-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="23788-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23788-107">dispidMeetingType</span><span class="sxs-lookup"><span data-stu-id="23788-107">dispidMeetingType</span></span>  <br/> |
|<span data-ttu-id="23788-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="23788-108">Property set:</span></span>  <br/> |<span data-ttu-id="23788-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="23788-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="23788-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="23788-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="23788-111">0x00000026</span><span class="sxs-lookup"><span data-stu-id="23788-111">0x00000026</span></span>  <br/> |
|<span data-ttu-id="23788-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="23788-112">Data type:</span></span>  <br/> |<span data-ttu-id="23788-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23788-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23788-114">Área:</span><span class="sxs-lookup"><span data-stu-id="23788-114">Area:</span></span>  <br/> |<span data-ttu-id="23788-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="23788-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23788-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="23788-116">Remarks</span></span>

<span data-ttu-id="23788-117">O valor dessa propriedade deve ser definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="23788-117">The value of this property must be set to one of the following:</span></span>
  
|<span data-ttu-id="23788-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="23788-118">**Property**</span></span>|<span data-ttu-id="23788-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="23788-119">**Value**</span></span>|<span data-ttu-id="23788-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="23788-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23788-121">mtgEmpty</span><span class="sxs-lookup"><span data-stu-id="23788-121">mtgEmpty</span></span>  <br/> |<span data-ttu-id="23788-122">0x00000000</span><span class="sxs-lookup"><span data-stu-id="23788-122">0x00000000</span></span>  <br/> |<span data-ttu-id="23788-123">Não especificado.</span><span class="sxs-lookup"><span data-stu-id="23788-123">Unspecified.</span></span>  <br/> |
|<span data-ttu-id="23788-124">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="23788-124">mtgRequest</span></span>  <br/> |<span data-ttu-id="23788-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="23788-125">0x00000001</span></span>  <br/> |<span data-ttu-id="23788-126">Solicitação de reunião inicial.</span><span class="sxs-lookup"><span data-stu-id="23788-126">Initial meeting request.</span></span>  <br/> |
|<span data-ttu-id="23788-127">mtgFull</span><span class="sxs-lookup"><span data-stu-id="23788-127">mtgFull</span></span>  <br/> |<span data-ttu-id="23788-128">0x00010000</span><span class="sxs-lookup"><span data-stu-id="23788-128">0x00010000</span></span>  <br/> |<span data-ttu-id="23788-129">Atualização completa.</span><span class="sxs-lookup"><span data-stu-id="23788-129">Full update.</span></span>  <br/> |
|<span data-ttu-id="23788-130">mtgInfo</span><span class="sxs-lookup"><span data-stu-id="23788-130">mtgInfo</span></span>  <br/> |<span data-ttu-id="23788-131">0x00020000</span><span class="sxs-lookup"><span data-stu-id="23788-131">0x00020000</span></span>  <br/> |<span data-ttu-id="23788-132">Atualização inFormativa.</span><span class="sxs-lookup"><span data-stu-id="23788-132">Informational update.</span></span>  <br/> |
|<span data-ttu-id="23788-133">mtgOutOfDate</span><span class="sxs-lookup"><span data-stu-id="23788-133">mtgOutOfDate</span></span>  <br/> |<span data-ttu-id="23788-134">0x00080000</span><span class="sxs-lookup"><span data-stu-id="23788-134">0x00080000</span></span>  <br/> |<span data-ttu-id="23788-135">Uma solicitação de reunião ou atualização de reunião mais recente foi recebida após esta.</span><span class="sxs-lookup"><span data-stu-id="23788-135">A newer meeting request or meeting update was received after this one.</span></span>  <br/> |
|<span data-ttu-id="23788-136">mtgDelegatorCopy</span><span class="sxs-lookup"><span data-stu-id="23788-136">mtgDelegatorCopy</span></span>  <br/> |<span data-ttu-id="23788-137">0x00100000</span><span class="sxs-lookup"><span data-stu-id="23788-137">0x00100000</span></span>  <br/> |<span data-ttu-id="23788-138">Isso é definido na cópia do delegante quando um representante manipula objetos relacionados à reunião.</span><span class="sxs-lookup"><span data-stu-id="23788-138">This is set on the delegator's copy when a delegate handles meeting-related objects.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="23788-139">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="23788-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23788-140">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="23788-140">Protocol specifications</span></span>

<span data-ttu-id="23788-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23788-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23788-142">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="23788-142">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23788-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23788-143">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23788-144">Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="23788-144">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23788-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23788-145">Header files</span></span>

<span data-ttu-id="23788-146">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="23788-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="23788-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="23788-147">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23788-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="23788-148">See also</span></span>



[<span data-ttu-id="23788-149">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="23788-149">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23788-150">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="23788-150">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23788-151">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="23788-151">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23788-152">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="23788-152">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


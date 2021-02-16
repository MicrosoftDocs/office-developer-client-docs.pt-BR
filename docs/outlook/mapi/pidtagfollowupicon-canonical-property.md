---
title: Propriedade canônica PidTagFollowupIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFollowupIcon
api_type:
- HeaderDef
ms.assetid: 374cef41-141a-491b-8dd1-eaf1a2044204
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 205b6ddc2b65297d69a2223aab7b745b223ee553
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316279"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="1887f-103">Propriedade canônica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="1887f-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="1887f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1887f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1887f-105">Especifica a cor do sinalizador do objeto message.</span><span class="sxs-lookup"><span data-stu-id="1887f-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1887f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1887f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1887f-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="1887f-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="1887f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1887f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1887f-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="1887f-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="1887f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1887f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1887f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1887f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1887f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1887f-112">Area:</span></span>  <br/> |<span data-ttu-id="1887f-113">Renomear pasta de mensagens</span><span class="sxs-lookup"><span data-stu-id="1887f-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1887f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1887f-114">Remarks</span></span>

<span data-ttu-id="1887f-115">Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) seja definido como "followupFlagged" ou o objeto message seja um objeto relacionado à reunião.</span><span class="sxs-lookup"><span data-stu-id="1887f-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="1887f-116">Essa propriedade não deve existir em um objeto task.</span><span class="sxs-lookup"><span data-stu-id="1887f-116">This property should not exist on a task object.</span></span> <span data-ttu-id="1887f-117">Quando definida em outros objetos de mensagem, essa propriedade deve ser definida como um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="1887f-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="1887f-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="1887f-118">**Numeric value**</span></span>|<span data-ttu-id="1887f-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1887f-119">**Name**</span></span>|<span data-ttu-id="1887f-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1887f-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1887f-121">Não presente</span><span class="sxs-lookup"><span data-stu-id="1887f-121">Not present</span></span>  <br/> |<span data-ttu-id="1887f-122">N/D</span><span class="sxs-lookup"><span data-stu-id="1887f-122">N/A</span></span>  <br/> |<span data-ttu-id="1887f-123">Sem cor</span><span class="sxs-lookup"><span data-stu-id="1887f-123">No color</span></span>  <br/> |
|<span data-ttu-id="1887f-124">1 </span><span class="sxs-lookup"><span data-stu-id="1887f-124">1</span></span>  <br/> |<span data-ttu-id="1887f-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="1887f-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="1887f-126">Sinalizador Roxo</span><span class="sxs-lookup"><span data-stu-id="1887f-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="1887f-127">2 </span><span class="sxs-lookup"><span data-stu-id="1887f-127">2</span></span>  <br/> |<span data-ttu-id="1887f-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="1887f-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="1887f-129">Sinalizador laranja</span><span class="sxs-lookup"><span data-stu-id="1887f-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="1887f-130">3 </span><span class="sxs-lookup"><span data-stu-id="1887f-130">3</span></span>  <br/> |<span data-ttu-id="1887f-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="1887f-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="1887f-132">Sinalizador verde</span><span class="sxs-lookup"><span data-stu-id="1887f-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="1887f-133">4 </span><span class="sxs-lookup"><span data-stu-id="1887f-133">4</span></span>  <br/> |<span data-ttu-id="1887f-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="1887f-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="1887f-135">Sinalizador amarelo</span><span class="sxs-lookup"><span data-stu-id="1887f-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="1887f-136">5 </span><span class="sxs-lookup"><span data-stu-id="1887f-136">5</span></span>  <br/> |<span data-ttu-id="1887f-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="1887f-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="1887f-138">Sinalizador azul</span><span class="sxs-lookup"><span data-stu-id="1887f-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="1887f-139">6 </span><span class="sxs-lookup"><span data-stu-id="1887f-139">6</span></span>  <br/> |<span data-ttu-id="1887f-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="1887f-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="1887f-141">Sinalizador vermelho</span><span class="sxs-lookup"><span data-stu-id="1887f-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1887f-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1887f-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1887f-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1887f-143">Protocol specifications</span></span>

<span data-ttu-id="1887f-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1887f-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1887f-145">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1887f-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1887f-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1887f-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1887f-147">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="1887f-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1887f-148">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1887f-148">Header files</span></span>

<span data-ttu-id="1887f-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1887f-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="1887f-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1887f-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="1887f-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1887f-151">Mapitags.h</span></span>
  
> <span data-ttu-id="1887f-152">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1887f-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1887f-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="1887f-153">See also</span></span>



[<span data-ttu-id="1887f-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1887f-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1887f-155">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1887f-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1887f-156">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1887f-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1887f-157">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1887f-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


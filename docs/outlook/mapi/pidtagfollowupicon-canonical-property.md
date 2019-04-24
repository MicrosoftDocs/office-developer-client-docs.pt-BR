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
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="ccbde-103">Propriedade canônica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="ccbde-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="ccbde-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccbde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccbde-105">Especifica a cor do sinalizador do objeto Message.</span><span class="sxs-lookup"><span data-stu-id="ccbde-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ccbde-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ccbde-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ccbde-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="ccbde-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="ccbde-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ccbde-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ccbde-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="ccbde-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="ccbde-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ccbde-110">Data type:</span></span>  <br/> |<span data-ttu-id="ccbde-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ccbde-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ccbde-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ccbde-112">Area:</span></span>  <br/> |<span data-ttu-id="ccbde-113">ReNomear pasta de mensagens</span><span class="sxs-lookup"><span data-stu-id="ccbde-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccbde-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccbde-114">Remarks</span></span>

<span data-ttu-id="ccbde-115">Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) seja definido como "followupFlagged" ou o objeto Message seja um objeto relacionado à reunião.</span><span class="sxs-lookup"><span data-stu-id="ccbde-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="ccbde-116">Esta propriedade não deve existir em um objeto Task.</span><span class="sxs-lookup"><span data-stu-id="ccbde-116">This property should not exist on a task object.</span></span> <span data-ttu-id="ccbde-117">Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccbde-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="ccbde-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="ccbde-118">**Numeric value**</span></span>|<span data-ttu-id="ccbde-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ccbde-119">**Name**</span></span>|<span data-ttu-id="ccbde-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ccbde-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccbde-121">Não está presente</span><span class="sxs-lookup"><span data-stu-id="ccbde-121">Not present</span></span>  <br/> |<span data-ttu-id="ccbde-122">N/D</span><span class="sxs-lookup"><span data-stu-id="ccbde-122">N/A</span></span>  <br/> |<span data-ttu-id="ccbde-123">Sem cor</span><span class="sxs-lookup"><span data-stu-id="ccbde-123">No color</span></span>  <br/> |
|<span data-ttu-id="ccbde-124">1</span><span class="sxs-lookup"><span data-stu-id="ccbde-124">1</span></span>  <br/> |<span data-ttu-id="ccbde-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="ccbde-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="ccbde-126">Sinalizador roxo</span><span class="sxs-lookup"><span data-stu-id="ccbde-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="ccbde-127">duas</span><span class="sxs-lookup"><span data-stu-id="ccbde-127">2</span></span>  <br/> |<span data-ttu-id="ccbde-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="ccbde-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="ccbde-129">Sinalizador laranja</span><span class="sxs-lookup"><span data-stu-id="ccbde-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="ccbde-130">3D</span><span class="sxs-lookup"><span data-stu-id="ccbde-130">3</span></span>  <br/> |<span data-ttu-id="ccbde-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="ccbde-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="ccbde-132">Sinalizador verde</span><span class="sxs-lookup"><span data-stu-id="ccbde-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="ccbde-133">quatro</span><span class="sxs-lookup"><span data-stu-id="ccbde-133">4</span></span>  <br/> |<span data-ttu-id="ccbde-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="ccbde-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="ccbde-135">Sinalizador amarelo</span><span class="sxs-lookup"><span data-stu-id="ccbde-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="ccbde-136">0,5</span><span class="sxs-lookup"><span data-stu-id="ccbde-136">5</span></span>  <br/> |<span data-ttu-id="ccbde-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="ccbde-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="ccbde-138">Sinalizador azul</span><span class="sxs-lookup"><span data-stu-id="ccbde-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="ccbde-139">6</span><span class="sxs-lookup"><span data-stu-id="ccbde-139">6</span></span>  <br/> |<span data-ttu-id="ccbde-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="ccbde-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="ccbde-141">Sinalizador vermelho</span><span class="sxs-lookup"><span data-stu-id="ccbde-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ccbde-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccbde-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ccbde-143">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ccbde-143">Protocol specifications</span></span>

<span data-ttu-id="ccbde-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ccbde-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ccbde-145">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ccbde-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ccbde-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ccbde-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ccbde-147">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="ccbde-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ccbde-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ccbde-148">Header files</span></span>

<span data-ttu-id="ccbde-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ccbde-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="ccbde-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ccbde-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="ccbde-151">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="ccbde-151">Mapitags.h</span></span>
  
> <span data-ttu-id="ccbde-152">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ccbde-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ccbde-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccbde-153">See also</span></span>



[<span data-ttu-id="ccbde-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ccbde-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ccbde-155">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ccbde-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ccbde-156">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ccbde-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ccbde-157">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ccbde-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


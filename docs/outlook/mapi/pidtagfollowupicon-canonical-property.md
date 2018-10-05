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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383517"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="3b976-103">Propriedade canônica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="3b976-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="3b976-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b976-105">Especifica a cor de sinalizador do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b976-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b976-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3b976-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b976-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="3b976-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="3b976-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3b976-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b976-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="3b976-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="3b976-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3b976-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b976-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3b976-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3b976-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3b976-112">Area:</span></span>  <br/> |<span data-ttu-id="3b976-113">Renomear pasta de mensagem</span><span class="sxs-lookup"><span data-stu-id="3b976-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b976-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b976-114">Remarks</span></span>

<span data-ttu-id="3b976-115">Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) é definido como "followupFlagged" ou a mensagem for um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="3b976-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="3b976-116">Essa propriedade não deve existir em um objeto task.</span><span class="sxs-lookup"><span data-stu-id="3b976-116">This property should not exist on a task object.</span></span> <span data-ttu-id="3b976-117">Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="3b976-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="3b976-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="3b976-118">**Numeric value**</span></span>|<span data-ttu-id="3b976-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3b976-119">**Name**</span></span>|<span data-ttu-id="3b976-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3b976-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3b976-121">Não estiver presente</span><span class="sxs-lookup"><span data-stu-id="3b976-121">Not present</span></span>  <br/> |<span data-ttu-id="3b976-122">N/A</span><span class="sxs-lookup"><span data-stu-id="3b976-122">N/A</span></span>  <br/> |<span data-ttu-id="3b976-123">Sem cor</span><span class="sxs-lookup"><span data-stu-id="3b976-123">No color</span></span>  <br/> |
|<span data-ttu-id="3b976-124">1</span><span class="sxs-lookup"><span data-stu-id="3b976-124">1</span></span>  <br/> |<span data-ttu-id="3b976-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="3b976-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="3b976-126">Sinalizador roxo</span><span class="sxs-lookup"><span data-stu-id="3b976-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="3b976-127">2</span><span class="sxs-lookup"><span data-stu-id="3b976-127">2</span></span>  <br/> |<span data-ttu-id="3b976-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="3b976-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="3b976-129">Sinalizador Laranja</span><span class="sxs-lookup"><span data-stu-id="3b976-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="3b976-130">3</span><span class="sxs-lookup"><span data-stu-id="3b976-130">3</span></span>  <br/> |<span data-ttu-id="3b976-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="3b976-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="3b976-132">Sinalizador verde</span><span class="sxs-lookup"><span data-stu-id="3b976-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="3b976-133">4</span><span class="sxs-lookup"><span data-stu-id="3b976-133">4</span></span>  <br/> |<span data-ttu-id="3b976-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="3b976-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="3b976-135">Sinalizador amarelo</span><span class="sxs-lookup"><span data-stu-id="3b976-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="3b976-136">5</span><span class="sxs-lookup"><span data-stu-id="3b976-136">5</span></span>  <br/> |<span data-ttu-id="3b976-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="3b976-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="3b976-138">Sinalizador azul</span><span class="sxs-lookup"><span data-stu-id="3b976-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="3b976-139">6</span><span class="sxs-lookup"><span data-stu-id="3b976-139">6</span></span>  <br/> |<span data-ttu-id="3b976-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="3b976-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="3b976-141">Sinalizador vermelho</span><span class="sxs-lookup"><span data-stu-id="3b976-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3b976-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b976-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b976-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3b976-143">Protocol specifications</span></span>

<span data-ttu-id="3b976-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b976-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b976-145">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3b976-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b976-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b976-146">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b976-147">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="3b976-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b976-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3b976-148">Header files</span></span>

<span data-ttu-id="3b976-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b976-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b976-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3b976-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b976-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3b976-151">Mapitags.h</span></span>
  
> <span data-ttu-id="3b976-152">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3b976-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b976-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b976-153">See also</span></span>



[<span data-ttu-id="3b976-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3b976-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b976-155">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3b976-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b976-156">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3b976-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b976-157">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3b976-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


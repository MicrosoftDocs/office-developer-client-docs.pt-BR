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
ms.openlocfilehash: 8fa96736b5404d84c6ab48851b916c5ab987ae2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593918"
---
# <a name="pidtagfollowupicon-canonical-property"></a><span data-ttu-id="8c2c2-103">Propriedade canônica PidTagFollowupIcon</span><span class="sxs-lookup"><span data-stu-id="8c2c2-103">PidTagFollowupIcon Canonical Property</span></span>

  
  
<span data-ttu-id="8c2c2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c2c2-105">Especifica a cor de sinalizador do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-105">Specifies the flag color of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8c2c2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c2c2-107">PR_FOLLOWUP_ICON</span><span class="sxs-lookup"><span data-stu-id="8c2c2-107">PR_FOLLOWUP_ICON</span></span>  <br/> |
|<span data-ttu-id="8c2c2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c2c2-109">0x1095</span><span class="sxs-lookup"><span data-stu-id="8c2c2-109">0x1095</span></span>  <br/> |
|<span data-ttu-id="8c2c2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c2c2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c2c2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c2c2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-112">Area:</span></span>  <br/> |<span data-ttu-id="8c2c2-113">Renomear pasta de mensagem</span><span class="sxs-lookup"><span data-stu-id="8c2c2-113">Rename message folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c2c2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c2c2-114">Remarks</span></span>

<span data-ttu-id="8c2c2-115">Essa propriedade não deve existir, a menos que o valor da propriedade **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) é definido como "followupFlagged" ou a mensagem for um objeto de reuniões.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-115">This property must not exist unless the value of the **PR_FLAG_STATUS** ([PidTagFlagStatus](pidtagflagstatus-canonical-property.md)) property is set to "followupFlagged", or the message object is a meeting-related object.</span></span> <span data-ttu-id="8c2c2-116">Essa propriedade não deve existir em um objeto task.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-116">This property should not exist on a task object.</span></span> <span data-ttu-id="8c2c2-117">Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-117">When set on other message objects, this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="8c2c2-118">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="8c2c2-118">**Numeric value**</span></span>|<span data-ttu-id="8c2c2-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8c2c2-119">**Name**</span></span>|<span data-ttu-id="8c2c2-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8c2c2-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8c2c2-121">Não estiver presente</span><span class="sxs-lookup"><span data-stu-id="8c2c2-121">Not present</span></span>  <br/> |<span data-ttu-id="8c2c2-122">N/A</span><span class="sxs-lookup"><span data-stu-id="8c2c2-122">N/A</span></span>  <br/> |<span data-ttu-id="8c2c2-123">Sem cor</span><span class="sxs-lookup"><span data-stu-id="8c2c2-123">No color</span></span>  <br/> |
|<span data-ttu-id="8c2c2-124">1</span><span class="sxs-lookup"><span data-stu-id="8c2c2-124">1</span></span>  <br/> |<span data-ttu-id="8c2c2-125">followupIcon1</span><span class="sxs-lookup"><span data-stu-id="8c2c2-125">followupIcon1</span></span>  <br/> |<span data-ttu-id="8c2c2-126">Sinalizador roxo</span><span class="sxs-lookup"><span data-stu-id="8c2c2-126">Purple flag</span></span>  <br/> |
|<span data-ttu-id="8c2c2-127">2</span><span class="sxs-lookup"><span data-stu-id="8c2c2-127">2</span></span>  <br/> |<span data-ttu-id="8c2c2-128">followupIcon2</span><span class="sxs-lookup"><span data-stu-id="8c2c2-128">followupIcon2</span></span>  <br/> |<span data-ttu-id="8c2c2-129">Sinalizador Laranja</span><span class="sxs-lookup"><span data-stu-id="8c2c2-129">Orange flag</span></span>  <br/> |
|<span data-ttu-id="8c2c2-130">3</span><span class="sxs-lookup"><span data-stu-id="8c2c2-130">3</span></span>  <br/> |<span data-ttu-id="8c2c2-131">followupIcon3</span><span class="sxs-lookup"><span data-stu-id="8c2c2-131">followupIcon3</span></span>  <br/> |<span data-ttu-id="8c2c2-132">Sinalizador verde</span><span class="sxs-lookup"><span data-stu-id="8c2c2-132">Green flag</span></span>  <br/> |
|<span data-ttu-id="8c2c2-133">4</span><span class="sxs-lookup"><span data-stu-id="8c2c2-133">4</span></span>  <br/> |<span data-ttu-id="8c2c2-134">followupIcon4</span><span class="sxs-lookup"><span data-stu-id="8c2c2-134">followupIcon4</span></span>  <br/> |<span data-ttu-id="8c2c2-135">Sinalizador amarelo</span><span class="sxs-lookup"><span data-stu-id="8c2c2-135">Yellow flag</span></span>  <br/> |
|<span data-ttu-id="8c2c2-136">5</span><span class="sxs-lookup"><span data-stu-id="8c2c2-136">5</span></span>  <br/> |<span data-ttu-id="8c2c2-137">followupIcon5</span><span class="sxs-lookup"><span data-stu-id="8c2c2-137">followupIcon5</span></span>  <br/> |<span data-ttu-id="8c2c2-138">Sinalizador azul</span><span class="sxs-lookup"><span data-stu-id="8c2c2-138">Blue flag</span></span>  <br/> |
|<span data-ttu-id="8c2c2-139">6</span><span class="sxs-lookup"><span data-stu-id="8c2c2-139">6</span></span>  <br/> |<span data-ttu-id="8c2c2-140">followupIcon6</span><span class="sxs-lookup"><span data-stu-id="8c2c2-140">followupIcon6</span></span>  <br/> |<span data-ttu-id="8c2c2-141">Sinalizador vermelho</span><span class="sxs-lookup"><span data-stu-id="8c2c2-141">Red flag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="8c2c2-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c2c2-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c2c2-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8c2c2-143">Protocol specifications</span></span>

<span data-ttu-id="8c2c2-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c2c2-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c2c2-145">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c2c2-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c2c2-146">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c2c2-147">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-147">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c2c2-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c2c2-148">Header files</span></span>

<span data-ttu-id="8c2c2-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c2c2-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c2c2-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-150">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c2c2-151">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c2c2-151">Mapitags.h</span></span>
  
> <span data-ttu-id="8c2c2-152">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-152">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c2c2-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c2c2-153">See also</span></span>



[<span data-ttu-id="8c2c2-154">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8c2c2-154">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c2c2-155">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="8c2c2-155">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c2c2-156">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8c2c2-156">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c2c2-157">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8c2c2-157">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


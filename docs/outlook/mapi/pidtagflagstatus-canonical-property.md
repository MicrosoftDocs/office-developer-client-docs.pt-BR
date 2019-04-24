---
title: Propriedade canônica PidTagFlagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFlagStatus
api_type:
- HeaderDef
ms.assetid: b5117360-0939-4535-83fe-3b4a240b5217
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bca8fccaa43bb3157b3d4e2af7d6aafa64972b41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316293"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="3089b-103">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="3089b-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="3089b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3089b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3089b-105">Especifica o estado de sinalizador do objeto Message.</span><span class="sxs-lookup"><span data-stu-id="3089b-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3089b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3089b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3089b-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="3089b-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="3089b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3089b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3089b-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="3089b-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="3089b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3089b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3089b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3089b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3089b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3089b-112">Area:</span></span>  <br/> |<span data-ttu-id="3089b-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="3089b-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3089b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3089b-114">Remarks</span></span>

<span data-ttu-id="3089b-115">Essa propriedade não deve existir em um objeto relacionado à reunião e não deve existir em um objeto Task.</span><span class="sxs-lookup"><span data-stu-id="3089b-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="3089b-116">Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3089b-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="3089b-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="3089b-117">**Numeric value**</span></span>|<span data-ttu-id="3089b-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3089b-118">**Name**</span></span>|<span data-ttu-id="3089b-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3089b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3089b-120">Não está presente</span><span class="sxs-lookup"><span data-stu-id="3089b-120">Not present</span></span>  <br/> |<span data-ttu-id="3089b-121">N/D</span><span class="sxs-lookup"><span data-stu-id="3089b-121">N/A</span></span>  <br/> |<span data-ttu-id="3089b-122">Não sinalizado</span><span class="sxs-lookup"><span data-stu-id="3089b-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="3089b-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3089b-123">0x00000001</span></span>  <br/> |<span data-ttu-id="3089b-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="3089b-124">followupComplete</span></span>  <br/> |<span data-ttu-id="3089b-125">Sinalizador concluído</span><span class="sxs-lookup"><span data-stu-id="3089b-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="3089b-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3089b-126">0x00000002</span></span>  <br/> |<span data-ttu-id="3089b-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="3089b-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="3089b-128">Indicado</span><span class="sxs-lookup"><span data-stu-id="3089b-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3089b-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3089b-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3089b-130">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3089b-130">Protocol specifications</span></span>

<span data-ttu-id="3089b-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3089b-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3089b-132">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3089b-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3089b-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3089b-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3089b-134">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="3089b-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3089b-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3089b-135">Header files</span></span>

<span data-ttu-id="3089b-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3089b-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="3089b-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3089b-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="3089b-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3089b-138">Mapitags.h</span></span>
  
> <span data-ttu-id="3089b-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3089b-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3089b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3089b-140">See also</span></span>



[<span data-ttu-id="3089b-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3089b-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3089b-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3089b-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3089b-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3089b-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3089b-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3089b-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="64d1f-103">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="64d1f-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="64d1f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64d1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64d1f-105">Especifica o estado do sinalizador do objeto message.</span><span class="sxs-lookup"><span data-stu-id="64d1f-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64d1f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="64d1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64d1f-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="64d1f-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="64d1f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="64d1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="64d1f-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="64d1f-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="64d1f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="64d1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="64d1f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="64d1f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="64d1f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="64d1f-112">Area:</span></span>  <br/> |<span data-ttu-id="64d1f-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="64d1f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64d1f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="64d1f-114">Remarks</span></span>

<span data-ttu-id="64d1f-115">Essa propriedade não deve existir em um objeto relacionado à reunião e não deve existir em um objeto de tarefa.</span><span class="sxs-lookup"><span data-stu-id="64d1f-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="64d1f-116">Quando definida em outros objetos de mensagem, essa propriedade deve ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="64d1f-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="64d1f-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="64d1f-117">**Numeric value**</span></span>|<span data-ttu-id="64d1f-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="64d1f-118">**Name**</span></span>|<span data-ttu-id="64d1f-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="64d1f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="64d1f-120">Não presente</span><span class="sxs-lookup"><span data-stu-id="64d1f-120">Not present</span></span>  <br/> |<span data-ttu-id="64d1f-121">N/D</span><span class="sxs-lookup"><span data-stu-id="64d1f-121">N/A</span></span>  <br/> |<span data-ttu-id="64d1f-122">Unflagged</span><span class="sxs-lookup"><span data-stu-id="64d1f-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="64d1f-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="64d1f-123">0x00000001</span></span>  <br/> |<span data-ttu-id="64d1f-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="64d1f-124">followupComplete</span></span>  <br/> |<span data-ttu-id="64d1f-125">Sinalizado concluído</span><span class="sxs-lookup"><span data-stu-id="64d1f-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="64d1f-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="64d1f-126">0x00000002</span></span>  <br/> |<span data-ttu-id="64d1f-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="64d1f-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="64d1f-128">Sinalizado</span><span class="sxs-lookup"><span data-stu-id="64d1f-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="64d1f-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64d1f-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64d1f-130">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="64d1f-130">Protocol specifications</span></span>

<span data-ttu-id="64d1f-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64d1f-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64d1f-132">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="64d1f-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64d1f-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64d1f-133">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64d1f-134">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="64d1f-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64d1f-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="64d1f-135">Header files</span></span>

<span data-ttu-id="64d1f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64d1f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="64d1f-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="64d1f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="64d1f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="64d1f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="64d1f-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="64d1f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64d1f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="64d1f-140">See also</span></span>



[<span data-ttu-id="64d1f-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64d1f-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64d1f-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="64d1f-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64d1f-143">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="64d1f-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64d1f-144">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="64d1f-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


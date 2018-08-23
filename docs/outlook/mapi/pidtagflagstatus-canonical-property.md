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
ms.openlocfilehash: 8dba5906a00beb6d38e4f3e375a9c57db79d42f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575956"
---
# <a name="pidtagflagstatus-canonical-property"></a><span data-ttu-id="5f856-103">Propriedade canônica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="5f856-103">PidTagFlagStatus Canonical Property</span></span>

  
  
<span data-ttu-id="5f856-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f856-105">Especifica o estado de sinalizador do objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5f856-105">Specifies the flag state of the message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f856-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5f856-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5f856-107">PR_FLAG_STATUS</span><span class="sxs-lookup"><span data-stu-id="5f856-107">PR_FLAG_STATUS</span></span>  <br/> |
|<span data-ttu-id="5f856-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5f856-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5f856-109">0x1090</span><span class="sxs-lookup"><span data-stu-id="5f856-109">0x1090</span></span>  <br/> |
|<span data-ttu-id="5f856-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5f856-110">Data type:</span></span>  <br/> |<span data-ttu-id="5f856-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5f856-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5f856-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5f856-112">Area:</span></span>  <br/> |<span data-ttu-id="5f856-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="5f856-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f856-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f856-114">Remarks</span></span>

<span data-ttu-id="5f856-115">Essa propriedade não deve existir em um objeto de reuniões e ele não deve existir em um objeto task.</span><span class="sxs-lookup"><span data-stu-id="5f856-115">This property must not exist on a meeting-related object, and it should not exist on a task object.</span></span> <span data-ttu-id="5f856-116">Quando definido em outros objetos de mensagem, essa propriedade deve ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5f856-116">When set on other message objects, this property must be set to one of the following values:</span></span>
  
|<span data-ttu-id="5f856-117">**Valor numérico**</span><span class="sxs-lookup"><span data-stu-id="5f856-117">**Numeric value**</span></span>|<span data-ttu-id="5f856-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5f856-118">**Name**</span></span>|<span data-ttu-id="5f856-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5f856-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5f856-120">Não estiver presente</span><span class="sxs-lookup"><span data-stu-id="5f856-120">Not present</span></span>  <br/> |<span data-ttu-id="5f856-121">N/A</span><span class="sxs-lookup"><span data-stu-id="5f856-121">N/A</span></span>  <br/> |<span data-ttu-id="5f856-122">Sem sinalizador</span><span class="sxs-lookup"><span data-stu-id="5f856-122">Unflagged</span></span>  <br/> |
|<span data-ttu-id="5f856-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f856-123">0x00000001</span></span>  <br/> |<span data-ttu-id="5f856-124">followupComplete</span><span class="sxs-lookup"><span data-stu-id="5f856-124">followupComplete</span></span>  <br/> |<span data-ttu-id="5f856-125">Sinalizado concluído</span><span class="sxs-lookup"><span data-stu-id="5f856-125">Flagged complete</span></span>  <br/> |
|<span data-ttu-id="5f856-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f856-126">0x00000002</span></span>  <br/> |<span data-ttu-id="5f856-127">followupFlagged</span><span class="sxs-lookup"><span data-stu-id="5f856-127">followupFlagged</span></span>  <br/> |<span data-ttu-id="5f856-128">Sinalizado</span><span class="sxs-lookup"><span data-stu-id="5f856-128">Flagged</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5f856-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f856-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5f856-130">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5f856-130">Protocol specifications</span></span>

<span data-ttu-id="5f856-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f856-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f856-132">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5f856-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5f856-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5f856-133">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5f856-134">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="5f856-134">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5f856-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5f856-135">Header files</span></span>

<span data-ttu-id="5f856-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5f856-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="5f856-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5f856-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="5f856-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5f856-138">Mapitags.h</span></span>
  
> <span data-ttu-id="5f856-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="5f856-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5f856-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f856-140">See also</span></span>



[<span data-ttu-id="5f856-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5f856-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5f856-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5f856-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5f856-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5f856-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5f856-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5f856-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


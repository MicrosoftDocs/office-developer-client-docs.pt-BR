---
title: Propriedade canônica PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385694"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="51ce2-103">Propriedade canônica PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="51ce2-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="51ce2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51ce2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51ce2-105">Controla como um objeto de mensagem é manipulado pelo cliente quando atuando na entrada do usuário final.</span><span class="sxs-lookup"><span data-stu-id="51ce2-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51ce2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="51ce2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51ce2-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="51ce2-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="51ce2-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="51ce2-108">Property set:</span></span>  <br/> |<span data-ttu-id="51ce2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="51ce2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="51ce2-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="51ce2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51ce2-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="51ce2-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="51ce2-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="51ce2-112">Data type:</span></span>  <br/> |<span data-ttu-id="51ce2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="51ce2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="51ce2-114">Área:</span><span class="sxs-lookup"><span data-stu-id="51ce2-114">Area:</span></span>  <br/> |<span data-ttu-id="51ce2-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="51ce2-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51ce2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ce2-116">Remarks</span></span>

<span data-ttu-id="51ce2-117">Deve ser definido como um bit a bit ou zero ou mais dos seguintes sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="51ce2-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="51ce2-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="51ce2-118">**Name**</span></span>|<span data-ttu-id="51ce2-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="51ce2-119">**Value**</span></span>|<span data-ttu-id="51ce2-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51ce2-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51ce2-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="51ce2-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="51ce2-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="51ce2-122">0x0001</span></span>  <br/> |<span data-ttu-id="51ce2-123">Processamento adicional é necessária no objeto mensagem ao excluir.</span><span class="sxs-lookup"><span data-stu-id="51ce2-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="51ce2-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="51ce2-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="51ce2-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="51ce2-125">0x0008</span></span>  <br/> |<span data-ttu-id="51ce2-126">Nenhuma interface de usuário está associado com o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="51ce2-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="51ce2-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="51ce2-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="51ce2-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="51ce2-128">0x0010</span></span>  <br/> |<span data-ttu-id="51ce2-129">Processamento adicional é necessária no objeto mensagem ao mover ou copiar a um objeto de pasta com uma propriedade **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "Falha de página inválida. Observe".</span><span class="sxs-lookup"><span data-stu-id="51ce2-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="51ce2-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="51ce2-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="51ce2-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="51ce2-131">0x0020</span></span>  <br/> |<span data-ttu-id="51ce2-132">Processamento adicional é necessária no objeto mensagem ao copiar para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="51ce2-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="51ce2-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="51ce2-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="51ce2-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="51ce2-134">0x0040</span></span>  <br/> |<span data-ttu-id="51ce2-135">Processamento adicional é necessária no objeto mensagem durante a mudança para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="51ce2-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="51ce2-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="51ce2-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="51ce2-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="51ce2-137">0x0100</span></span>  <br/> |<span data-ttu-id="51ce2-138">Processamento adicional é necessária no objeto mensagem ao exibir os verbos para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="51ce2-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="51ce2-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="51ce2-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="51ce2-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="51ce2-140">0x0400</span></span>  <br/> |<span data-ttu-id="51ce2-141">Não é possível desfazer a operação de exclusão, não deve ser definida, a menos que "seOpenToDelete" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="51ce2-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="51ce2-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="51ce2-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="51ce2-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="51ce2-143">0x0800</span></span>  <br/> |<span data-ttu-id="51ce2-144">Não é possível desfazer a operação de cópia, não deve ser definida, a menos que "seOpenTocopy" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="51ce2-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="51ce2-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="51ce2-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="51ce2-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="51ce2-146">0x1000</span></span>  <br/> |<span data-ttu-id="51ce2-147">Não é possível desfazer a operação de movimentação, não deve ser definida, a menos que "seOpenToMove" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="51ce2-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="51ce2-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="51ce2-148">seHasScript</span></span>  <br/> |<span data-ttu-id="51ce2-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="51ce2-149">0x2000</span></span>  <br/> |<span data-ttu-id="51ce2-150">O objeto de mensagem contém um script do usuário final.</span><span class="sxs-lookup"><span data-stu-id="51ce2-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="51ce2-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="51ce2-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="51ce2-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="51ce2-152">0x4000</span></span>  <br/> |<span data-ttu-id="51ce2-153">Processamento adicional é necessária para excluir permanentemente o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="51ce2-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="51ce2-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="51ce2-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51ce2-155">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="51ce2-155">Protocol specifications</span></span>

<span data-ttu-id="51ce2-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51ce2-156">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51ce2-157">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="51ce2-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51ce2-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51ce2-158">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51ce2-159">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="51ce2-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="51ce2-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51ce2-160">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51ce2-161">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="51ce2-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51ce2-162">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51ce2-162">Header files</span></span>

<span data-ttu-id="51ce2-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51ce2-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="51ce2-164">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="51ce2-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51ce2-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="51ce2-165">See also</span></span>



[<span data-ttu-id="51ce2-166">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="51ce2-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51ce2-167">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="51ce2-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51ce2-168">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="51ce2-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51ce2-169">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="51ce2-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


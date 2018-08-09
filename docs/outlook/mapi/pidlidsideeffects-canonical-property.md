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
ms.openlocfilehash: 479ba1990f7cac1768fc5e514e3fc55f017e4a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768653"
---
# <a name="pidlidsideeffects-canonical-property"></a><span data-ttu-id="13d24-103">Propriedade canônica PidLidSideEffects</span><span class="sxs-lookup"><span data-stu-id="13d24-103">PidLidSideEffects Canonical Property</span></span>

  
  
<span data-ttu-id="13d24-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13d24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13d24-105">Controla como um objeto de mensagem é manipulado pelo cliente quando atuando na entrada do usuário final.</span><span class="sxs-lookup"><span data-stu-id="13d24-105">Controls how a message object is handled by the client when acting on end-user input.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13d24-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="13d24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13d24-107">dispidSideEffects</span><span class="sxs-lookup"><span data-stu-id="13d24-107">dispidSideEffects</span></span>  <br/> |
|<span data-ttu-id="13d24-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="13d24-108">Property set:</span></span>  <br/> |<span data-ttu-id="13d24-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="13d24-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="13d24-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="13d24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13d24-111">0x00008510</span><span class="sxs-lookup"><span data-stu-id="13d24-111">0x00008510</span></span>  <br/> |
|<span data-ttu-id="13d24-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="13d24-112">Data type:</span></span>  <br/> |<span data-ttu-id="13d24-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="13d24-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="13d24-114">Área:</span><span class="sxs-lookup"><span data-stu-id="13d24-114">Area:</span></span>  <br/> |<span data-ttu-id="13d24-115">Configuração de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="13d24-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13d24-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d24-116">Remarks</span></span>

<span data-ttu-id="13d24-117">Deve ser definido como um bit a bit ou zero ou mais dos seguintes sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="13d24-117">Must be set to a bitwise or zero or more of the following flags.</span></span>
  
|<span data-ttu-id="13d24-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="13d24-118">**Name**</span></span>|<span data-ttu-id="13d24-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="13d24-119">**Value**</span></span>|<span data-ttu-id="13d24-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="13d24-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13d24-121">seOpenToDelete</span><span class="sxs-lookup"><span data-stu-id="13d24-121">seOpenToDelete</span></span>  <br/> |<span data-ttu-id="13d24-122">0x0001</span><span class="sxs-lookup"><span data-stu-id="13d24-122">0x0001</span></span>  <br/> |<span data-ttu-id="13d24-123">Processamento adicional é necessária no objeto mensagem ao excluir.</span><span class="sxs-lookup"><span data-stu-id="13d24-123">Additional processing is required on the message object when deleting.</span></span>  <br/> |
|<span data-ttu-id="13d24-124">seNoFrame</span><span class="sxs-lookup"><span data-stu-id="13d24-124">seNoFrame</span></span>  <br/> |<span data-ttu-id="13d24-125">0x0008</span><span class="sxs-lookup"><span data-stu-id="13d24-125">0x0008</span></span>  <br/> |<span data-ttu-id="13d24-126">Nenhuma interface de usuário está associado com o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="13d24-126">No UI is associated with the message object.</span></span>  <br/> |
|<span data-ttu-id="13d24-127">seCoerceToInbox</span><span class="sxs-lookup"><span data-stu-id="13d24-127">seCoerceToInbox</span></span>  <br/> |<span data-ttu-id="13d24-128">0x0010</span><span class="sxs-lookup"><span data-stu-id="13d24-128">0x0010</span></span>  <br/> |<span data-ttu-id="13d24-129">Processamento adicional é necessária no objeto mensagem ao mover ou copiar a um objeto de pasta com uma propriedade **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de "Falha de página inválida. Observe".</span><span class="sxs-lookup"><span data-stu-id="13d24-129">Additional processing is required on the message object when moving or copying to a folder object with a **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) property of "IPF.Note".</span></span>  <br/> |
|<span data-ttu-id="13d24-130">seOpenTocopy</span><span class="sxs-lookup"><span data-stu-id="13d24-130">seOpenTocopy</span></span>  <br/> |<span data-ttu-id="13d24-131">0x0020</span><span class="sxs-lookup"><span data-stu-id="13d24-131">0x0020</span></span>  <br/> |<span data-ttu-id="13d24-132">Processamento adicional é necessária no objeto mensagem ao copiar para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="13d24-132">Additional processing is required on the message object when copying to another folder.</span></span>  <br/> |
|<span data-ttu-id="13d24-133">seOpenToMove</span><span class="sxs-lookup"><span data-stu-id="13d24-133">seOpenToMove</span></span>  <br/> |<span data-ttu-id="13d24-134">0x0040</span><span class="sxs-lookup"><span data-stu-id="13d24-134">0x0040</span></span>  <br/> |<span data-ttu-id="13d24-135">Processamento adicional é necessária no objeto mensagem durante a mudança para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="13d24-135">Additional processing is required on the message object when moving to another folder.</span></span>  <br/> |
|<span data-ttu-id="13d24-136">seOpenForCtxMenu</span><span class="sxs-lookup"><span data-stu-id="13d24-136">seOpenForCtxMenu</span></span>  <br/> |<span data-ttu-id="13d24-137">0x0100</span><span class="sxs-lookup"><span data-stu-id="13d24-137">0x0100</span></span>  <br/> |<span data-ttu-id="13d24-138">Processamento adicional é necessária no objeto mensagem ao exibir os verbos para o usuário final.</span><span class="sxs-lookup"><span data-stu-id="13d24-138">Additional processing is required on the message object when displaying verbs to the end-user.</span></span>  <br/> |
|<span data-ttu-id="13d24-139">seCannotUndoDelete</span><span class="sxs-lookup"><span data-stu-id="13d24-139">seCannotUndoDelete</span></span>  <br/> |<span data-ttu-id="13d24-140">0x0400</span><span class="sxs-lookup"><span data-stu-id="13d24-140">0x0400</span></span>  <br/> |<span data-ttu-id="13d24-141">Não é possível desfazer a operação de exclusão, não deve ser definida, a menos que "seOpenToDelete" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="13d24-141">Cannot undo delete operation, must not be set unless "seOpenToDelete" is set.</span></span>  <br/> |
|<span data-ttu-id="13d24-142">seCannotUndoCopy</span><span class="sxs-lookup"><span data-stu-id="13d24-142">seCannotUndoCopy</span></span>  <br/> |<span data-ttu-id="13d24-143">0x0800</span><span class="sxs-lookup"><span data-stu-id="13d24-143">0x0800</span></span>  <br/> |<span data-ttu-id="13d24-144">Não é possível desfazer a operação de cópia, não deve ser definida, a menos que "seOpenTocopy" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="13d24-144">Cannot undo copy operation, must not be set unless "seOpenTocopy" is set.</span></span>  <br/> |
|<span data-ttu-id="13d24-145">seCannotUndoMove</span><span class="sxs-lookup"><span data-stu-id="13d24-145">seCannotUndoMove</span></span>  <br/> |<span data-ttu-id="13d24-146">0x1000</span><span class="sxs-lookup"><span data-stu-id="13d24-146">0x1000</span></span>  <br/> |<span data-ttu-id="13d24-147">Não é possível desfazer a operação de movimentação, não deve ser definida, a menos que "seOpenToMove" estiver definida.</span><span class="sxs-lookup"><span data-stu-id="13d24-147">Cannot undo move operation, must not be set unless "seOpenToMove" is set.</span></span>  <br/> |
|<span data-ttu-id="13d24-148">seHasScript</span><span class="sxs-lookup"><span data-stu-id="13d24-148">seHasScript</span></span>  <br/> |<span data-ttu-id="13d24-149">0x2000</span><span class="sxs-lookup"><span data-stu-id="13d24-149">0x2000</span></span>  <br/> |<span data-ttu-id="13d24-150">O objeto de mensagem contém um script do usuário final.</span><span class="sxs-lookup"><span data-stu-id="13d24-150">The message object contains end-user script.</span></span>  <br/> |
|<span data-ttu-id="13d24-151">seOpenToPermDelete</span><span class="sxs-lookup"><span data-stu-id="13d24-151">seOpenToPermDelete</span></span>  <br/> |<span data-ttu-id="13d24-152">0x4000</span><span class="sxs-lookup"><span data-stu-id="13d24-152">0x4000</span></span>  <br/> |<span data-ttu-id="13d24-153">Processamento adicional é necessária para excluir permanentemente o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="13d24-153">Additional processing is required to permanently delete the message object.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="13d24-154">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13d24-154">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13d24-155">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="13d24-155">Protocol specifications</span></span>

<span data-ttu-id="13d24-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13d24-156">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13d24-157">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13d24-157">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13d24-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13d24-158">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13d24-159">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="13d24-159">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="13d24-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13d24-160">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13d24-161">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="13d24-161">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13d24-162">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13d24-162">Header files</span></span>

<span data-ttu-id="13d24-163">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13d24-163">Mapidefs.h</span></span>
  
> <span data-ttu-id="13d24-164">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="13d24-164">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13d24-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d24-165">See also</span></span>



[<span data-ttu-id="13d24-166">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13d24-166">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13d24-167">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="13d24-167">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13d24-168">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="13d24-168">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13d24-169">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="13d24-169">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


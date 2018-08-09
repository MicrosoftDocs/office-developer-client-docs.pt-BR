---
title: Propriedade canônica PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8ca8d7a82360c1f96448b08c9eda18be502b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768750"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="e404f-103">Propriedade canônica PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="e404f-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="e404f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e404f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e404f-105">Especifica o status do progresso do usuário na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e404f-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e404f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e404f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e404f-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="e404f-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="e404f-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e404f-108">Property set:</span></span>  <br/> |<span data-ttu-id="e404f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e404f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e404f-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e404f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e404f-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="e404f-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="e404f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e404f-112">Data type:</span></span>  <br/> |<span data-ttu-id="e404f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e404f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e404f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e404f-114">Area:</span></span>  <br/> |<span data-ttu-id="e404f-115">Task</span><span class="sxs-lookup"><span data-stu-id="e404f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e404f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e404f-116">Remarks</span></span>

<span data-ttu-id="e404f-117">O valor dessa propriedade deve ser definido como um destes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="e404f-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="e404f-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e404f-118">**Value**</span></span>|<span data-ttu-id="e404f-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e404f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e404f-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e404f-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e404f-121">O usuário não foi iniciada trabalho na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e404f-121">The user has not started work on the task.</span></span> <span data-ttu-id="e404f-122">Se esse valor for definido, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) deve ser 0,0.</span><span class="sxs-lookup"><span data-stu-id="e404f-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="e404f-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e404f-123">0x00000001</span></span>  <br/> |<span data-ttu-id="e404f-124">Trabalho do usuário nessa tarefa está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e404f-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="e404f-125">Se esse valor for definido, **dispidPercentComplete** deve ser maior que 0,0 e 1,0 menores.</span><span class="sxs-lookup"><span data-stu-id="e404f-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="e404f-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e404f-126">0x00000002</span></span>  <br/> |<span data-ttu-id="e404f-127">Trabalho do usuário nessa tarefa é concluído.</span><span class="sxs-lookup"><span data-stu-id="e404f-127">The user's work on this task is complete.</span></span> <span data-ttu-id="e404f-128">Se esse valor for definido, **dispidPercentComplete** deve ser 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) deve ser a data atual e **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) deve ser TRUE.</span><span class="sxs-lookup"><span data-stu-id="e404f-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="e404f-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e404f-129">0x00000003</span></span>  <br/> |<span data-ttu-id="e404f-130">O usuário está aguardando outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="e404f-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="e404f-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e404f-131">0x00000004</span></span>  <br/> |<span data-ttu-id="e404f-132">O usuário tem adiada trabalho na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e404f-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e404f-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e404f-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e404f-134">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e404f-134">Protocol specifications</span></span>

<span data-ttu-id="e404f-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-136">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e404f-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e404f-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-138">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e404f-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="e404f-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-140">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="e404f-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="e404f-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-142">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="e404f-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="e404f-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-144">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e404f-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e404f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-146">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="e404f-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e404f-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e404f-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e404f-148">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="e404f-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e404f-149">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e404f-149">Header files</span></span>

<span data-ttu-id="e404f-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e404f-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="e404f-151">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e404f-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e404f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="e404f-152">See also</span></span>



[<span data-ttu-id="e404f-153">Propriedade canônica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="e404f-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="e404f-154">Propriedade canônica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="e404f-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="e404f-155">Propriedade canônica PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="e404f-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="e404f-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e404f-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e404f-157">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e404f-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e404f-158">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e404f-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e404f-159">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e404f-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


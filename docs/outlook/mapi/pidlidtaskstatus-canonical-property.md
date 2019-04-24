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
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316664"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="017e5-103">Propriedade canônica PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="017e5-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="017e5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="017e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="017e5-105">Especifica o status do progresso do usuário na tarefa.</span><span class="sxs-lookup"><span data-stu-id="017e5-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="017e5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="017e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="017e5-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="017e5-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="017e5-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="017e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="017e5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="017e5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="017e5-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="017e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="017e5-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="017e5-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="017e5-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="017e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="017e5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="017e5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="017e5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="017e5-114">Area:</span></span>  <br/> |<span data-ttu-id="017e5-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="017e5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="017e5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="017e5-116">Remarks</span></span>

<span data-ttu-id="017e5-117">O valor dessa propriedade deve ser definido como um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="017e5-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="017e5-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="017e5-118">**Value**</span></span>|<span data-ttu-id="017e5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="017e5-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="017e5-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="017e5-120">0x00000000</span></span>  <br/> |<span data-ttu-id="017e5-121">O usuário não iniciou o trabalho na tarefa.</span><span class="sxs-lookup"><span data-stu-id="017e5-121">The user has not started work on the task.</span></span> <span data-ttu-id="017e5-122">Se esse valor for definido, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) deverá ser 0,0.</span><span class="sxs-lookup"><span data-stu-id="017e5-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="017e5-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="017e5-123">0x00000001</span></span>  <br/> |<span data-ttu-id="017e5-124">O trabalho do usuário nesta tarefa está em andamento.</span><span class="sxs-lookup"><span data-stu-id="017e5-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="017e5-125">Se esse valor for definido, **dispidPercentComplete** deve ser maior que 0,0 e menor que 1,0.</span><span class="sxs-lookup"><span data-stu-id="017e5-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="017e5-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="017e5-126">0x00000002</span></span>  <br/> |<span data-ttu-id="017e5-127">O trabalho do usuário nesta tarefa foi concluído.</span><span class="sxs-lookup"><span data-stu-id="017e5-127">The user's work on this task is complete.</span></span> <span data-ttu-id="017e5-128">Se esse valor for definido, **dispidPercentComplete** deverá ser 1,0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) deverá ser a data atual, e **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) deverá ser true.</span><span class="sxs-lookup"><span data-stu-id="017e5-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="017e5-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="017e5-129">0x00000003</span></span>  <br/> |<span data-ttu-id="017e5-130">O usuário está aguardando outra pessoa.</span><span class="sxs-lookup"><span data-stu-id="017e5-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="017e5-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="017e5-131">0x00000004</span></span>  <br/> |<span data-ttu-id="017e5-132">O usuário retardava o trabalho da tarefa.</span><span class="sxs-lookup"><span data-stu-id="017e5-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="017e5-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="017e5-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="017e5-134">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="017e5-134">Protocol specifications</span></span>

<span data-ttu-id="017e5-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-136">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="017e5-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="017e5-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-138">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="017e5-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="017e5-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-140">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="017e5-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="017e5-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-142">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="017e5-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="017e5-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-144">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="017e5-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="017e5-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-146">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="017e5-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="017e5-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="017e5-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="017e5-148">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="017e5-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="017e5-149">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="017e5-149">Header files</span></span>

<span data-ttu-id="017e5-150">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="017e5-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="017e5-151">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="017e5-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="017e5-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="017e5-152">See also</span></span>



[<span data-ttu-id="017e5-153">Propriedade canônica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="017e5-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="017e5-154">Propriedade canônica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="017e5-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="017e5-155">Propriedade canônica PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="017e5-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="017e5-156">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="017e5-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="017e5-157">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="017e5-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="017e5-158">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="017e5-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="017e5-159">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="017e5-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


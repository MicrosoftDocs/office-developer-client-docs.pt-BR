---
title: Propriedade canônica PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316531"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="7e3bc-103">Propriedade canônica PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="7e3bc-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="7e3bc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e3bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e3bc-105">Indica o estado de atribuição atual da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e3bc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7e3bc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e3bc-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="7e3bc-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="7e3bc-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="7e3bc-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e3bc-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7e3bc-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7e3bc-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="7e3bc-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e3bc-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="7e3bc-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="7e3bc-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7e3bc-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e3bc-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7e3bc-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7e3bc-114">Área:</span><span class="sxs-lookup"><span data-stu-id="7e3bc-114">Area:</span></span>  <br/> |<span data-ttu-id="7e3bc-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="7e3bc-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e3bc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e3bc-116">Remarks</span></span>

<span data-ttu-id="7e3bc-117">O valor dessa propriedade deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="7e3bc-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7e3bc-118">**Value**</span></span>|<span data-ttu-id="7e3bc-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7e3bc-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e3bc-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bc-120">0x00000000</span></span>  <br/> |<span data-ttu-id="7e3bc-121">Esta tarefa foi criada para corresponder a uma tarefa que foi incorporada a rejeição de tarefa, mas que não pôde ser encontrada localmente.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="7e3bc-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7e3bc-122">0x00000001</span></span>  <br/> |<span data-ttu-id="7e3bc-123">A tarefa não foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="7e3bc-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7e3bc-124">0x00000002</span></span>  <br/> |<span data-ttu-id="7e3bc-125">A tarefa é a cópia de uma tarefa atribuída do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="7e3bc-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="7e3bc-126">0x00000003</span></span>  <br/> |<span data-ttu-id="7e3bc-127">A tarefa é a cópia de uma tarefa atribuída do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="7e3bc-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7e3bc-128">0x00000004</span></span>  <br/> |<span data-ttu-id="7e3bc-129">A tarefa é a cópia de uma tarefa rejeitada do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7e3bc-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7e3bc-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e3bc-131">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="7e3bc-131">Protocol specifications</span></span>

<span data-ttu-id="7e3bc-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bc-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bc-133">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e3bc-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bc-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bc-135">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="7e3bc-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bc-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bc-137">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="7e3bc-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bc-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bc-139">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="7e3bc-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e3bc-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e3bc-141">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e3bc-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7e3bc-142">Header files</span></span>

<span data-ttu-id="7e3bc-143">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7e3bc-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e3bc-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7e3bc-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e3bc-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e3bc-145">See also</span></span>



[<span data-ttu-id="7e3bc-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bc-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e3bc-147">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bc-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e3bc-148">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7e3bc-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e3bc-149">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7e3bc-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


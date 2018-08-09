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
ms.openlocfilehash: b4bab1948bc563b92dafa16922da3b9760cf1a1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768733"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="e659d-103">Propriedade canônica PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="e659d-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="e659d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e659d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e659d-105">Indica o estado atual da atribuição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e659d-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e659d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e659d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e659d-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="e659d-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="e659d-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e659d-108">Property set:</span></span>  <br/> |<span data-ttu-id="e659d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e659d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e659d-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e659d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e659d-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="e659d-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="e659d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e659d-112">Data type:</span></span>  <br/> |<span data-ttu-id="e659d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e659d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e659d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e659d-114">Area:</span></span>  <br/> |<span data-ttu-id="e659d-115">Task</span><span class="sxs-lookup"><span data-stu-id="e659d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e659d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e659d-116">Remarks</span></span>

<span data-ttu-id="e659d-117">O valor dessa propriedade deve ser um destes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="e659d-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="e659d-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e659d-118">**Value**</span></span>|<span data-ttu-id="e659d-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e659d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e659d-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e659d-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e659d-121">Esta tarefa foi criada para corresponder a uma tarefa que foi incorporada a uma rejeição da tarefa, mas não pôde ser encontrada localmente.</span><span class="sxs-lookup"><span data-stu-id="e659d-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="e659d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e659d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e659d-123">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="e659d-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e659d-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e659d-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e659d-125">A tarefa é uma cópia do destinatário da tarefa de uma tarefa atribuída.</span><span class="sxs-lookup"><span data-stu-id="e659d-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="e659d-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e659d-126">0x00000003</span></span>  <br/> |<span data-ttu-id="e659d-127">A tarefa é uma cópia do cedente a tarefa de uma tarefa atribuída.</span><span class="sxs-lookup"><span data-stu-id="e659d-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="e659d-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e659d-128">0x00000004</span></span>  <br/> |<span data-ttu-id="e659d-129">A tarefa é uma cópia do cedente a tarefa de uma tarefa rejeitada.</span><span class="sxs-lookup"><span data-stu-id="e659d-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e659d-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e659d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e659d-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e659d-131">Protocol specifications</span></span>

<span data-ttu-id="e659d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e659d-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e659d-133">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e659d-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e659d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e659d-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e659d-135">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e659d-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="e659d-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e659d-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e659d-137">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="e659d-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="e659d-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e659d-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e659d-139">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="e659d-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e659d-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e659d-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e659d-141">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="e659d-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e659d-142">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e659d-142">Header files</span></span>

<span data-ttu-id="e659d-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e659d-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="e659d-144">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e659d-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e659d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="e659d-145">See also</span></span>



[<span data-ttu-id="e659d-146">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e659d-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e659d-147">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e659d-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e659d-148">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e659d-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e659d-149">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e659d-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


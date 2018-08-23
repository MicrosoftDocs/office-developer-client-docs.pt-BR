---
title: Propriedade canônica PidLidTaskMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578077"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="e3cb0-103">Propriedade canônica PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="e3cb0-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="e3cb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3cb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3cb0-105">Especifica o status de atribuição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3cb0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e3cb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3cb0-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="e3cb0-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="e3cb0-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e3cb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="e3cb0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e3cb0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e3cb0-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e3cb0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e3cb0-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="e3cb0-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="e3cb0-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e3cb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="e3cb0-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e3cb0-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e3cb0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e3cb0-114">Area:</span></span>  <br/> |<span data-ttu-id="e3cb0-115">Task</span><span class="sxs-lookup"><span data-stu-id="e3cb0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3cb0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3cb0-116">Remarks</span></span>

<span data-ttu-id="e3cb0-117">O valor deve ser um destes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="e3cb0-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e3cb0-118">**Value**</span></span>|<span data-ttu-id="e3cb0-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e3cb0-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3cb0-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e3cb0-120">0x00000000</span></span>  <br/> |<span data-ttu-id="e3cb0-121">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="e3cb0-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e3cb0-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e3cb0-123">A tarefa está incorporada em uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="e3cb0-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e3cb0-124">0x00000002</span></span>  <br/> |<span data-ttu-id="e3cb0-125">A tarefa foi aceita pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="e3cb0-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="e3cb0-126">0x00000003</span></span>  <br/> |<span data-ttu-id="e3cb0-127">A tarefa foi rejeitada pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="e3cb0-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e3cb0-128">0x00000004</span></span>  <br/> |<span data-ttu-id="e3cb0-129">A tarefa está incorporada em uma atualização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="e3cb0-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="e3cb0-130">0x00000005</span></span>  <br/> |<span data-ttu-id="e3cb0-131">A tarefa foi atribuída ao cedente a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e3cb0-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3cb0-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3cb0-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e3cb0-133">Protocol specifications</span></span>

<span data-ttu-id="e3cb0-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3cb0-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3cb0-135">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3cb0-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3cb0-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3cb0-137">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3cb0-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3cb0-138">Header files</span></span>

<span data-ttu-id="e3cb0-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3cb0-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3cb0-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e3cb0-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3cb0-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3cb0-141">See also</span></span>



[<span data-ttu-id="e3cb0-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e3cb0-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3cb0-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e3cb0-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3cb0-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e3cb0-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3cb0-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e3cb0-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


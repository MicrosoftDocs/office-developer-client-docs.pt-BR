---
title: Propriedade canônica PidLidTaskHistory
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskHistory
api_type:
- COM
ms.assetid: 104ef21c-b607-48b7-9b06-bc53b7d9b68a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ba900ec4b8c8f1bcc2c85aae6c78ab59a43ee3cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563622"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="349db-103">Propriedade canônica PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="349db-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="349db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="349db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="349db-105">Indica o tipo de alteração foi feita última para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="349db-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="349db-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="349db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="349db-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="349db-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="349db-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="349db-108">Property set:</span></span>  <br/> |<span data-ttu-id="349db-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="349db-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="349db-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="349db-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="349db-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="349db-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="349db-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="349db-112">Data type:</span></span>  <br/> |<span data-ttu-id="349db-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="349db-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="349db-114">Área:</span><span class="sxs-lookup"><span data-stu-id="349db-114">Area:</span></span>  <br/> |<span data-ttu-id="349db-115">Task</span><span class="sxs-lookup"><span data-stu-id="349db-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="349db-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="349db-116">Remarks</span></span>

<span data-ttu-id="349db-117">Quando o valor dessa propriedade é definido, a propriedade **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) também deve ser definida para a hora atual.</span><span class="sxs-lookup"><span data-stu-id="349db-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="349db-118">A tabela a seguir mostra o **dispidTaskHistory** valores de propriedade, listados em ordem decrescente de prioridade.</span><span class="sxs-lookup"><span data-stu-id="349db-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="349db-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="349db-119">**Value**</span></span>|<span data-ttu-id="349db-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="349db-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="349db-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="349db-121">0x00000004</span></span>  <br/> |<span data-ttu-id="349db-122">A propriedade de **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) foi alterada.</span><span class="sxs-lookup"><span data-stu-id="349db-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="349db-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="349db-123">0x00000003</span></span>  <br/> |<span data-ttu-id="349db-124">Outra propriedade foi alterada.</span><span class="sxs-lookup"><span data-stu-id="349db-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="349db-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="349db-125">0x00000001</span></span>  <br/> |<span data-ttu-id="349db-126">O destinatário da tarefa aceita essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="349db-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="349db-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="349db-127">0x00000002</span></span>  <br/> |<span data-ttu-id="349db-128">O destinatário da tarefa rejeitada essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="349db-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="349db-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="349db-129">0x00000005</span></span>  <br/> |<span data-ttu-id="349db-130">A tarefa foi atribuída a um destinatário de tarefa.</span><span class="sxs-lookup"><span data-stu-id="349db-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="349db-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="349db-131">0x00000000</span></span>  <br/> |<span data-ttu-id="349db-132">Nenhuma alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="349db-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="349db-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="349db-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="349db-134">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="349db-134">Protocol specifications</span></span>

<span data-ttu-id="349db-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="349db-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="349db-136">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="349db-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="349db-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="349db-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="349db-138">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="349db-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="349db-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="349db-139">Header files</span></span>

<span data-ttu-id="349db-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="349db-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="349db-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="349db-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="349db-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="349db-142">See also</span></span>



[<span data-ttu-id="349db-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="349db-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="349db-144">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="349db-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="349db-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="349db-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="349db-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="349db-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


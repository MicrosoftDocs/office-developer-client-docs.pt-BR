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
ms.openlocfilehash: 39f2e6aeb4026f0b33be08b3bd8123283e5df3e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303007"
---
# <a name="pidlidtaskhistory-canonical-property"></a><span data-ttu-id="ec638-103">Propriedade canônica PidLidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="ec638-103">PidLidTaskHistory Canonical Property</span></span>

  
  
<span data-ttu-id="ec638-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec638-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec638-105">Indica o tipo de alteração que foi feita pela última vez na tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec638-105">Indicates the type of change that was last made to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec638-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ec638-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec638-107">dispidTaskHistory</span><span class="sxs-lookup"><span data-stu-id="ec638-107">dispidTaskHistory</span></span>  <br/> |
|<span data-ttu-id="ec638-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ec638-108">Property set:</span></span>  <br/> |<span data-ttu-id="ec638-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ec638-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ec638-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ec638-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ec638-111">0x0000811A</span><span class="sxs-lookup"><span data-stu-id="ec638-111">0x0000811A</span></span>  <br/> |
|<span data-ttu-id="ec638-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ec638-112">Data type:</span></span>  <br/> |<span data-ttu-id="ec638-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ec638-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ec638-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ec638-114">Area:</span></span>  <br/> |<span data-ttu-id="ec638-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="ec638-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec638-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec638-116">Remarks</span></span>

<span data-ttu-id="ec638-117">Quando o valor dessa propriedade é definido, a propriedade **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) também deve ser definida como a hora atual.</span><span class="sxs-lookup"><span data-stu-id="ec638-117">When the value of this property is set, the **dispidTaskLastUpdate** ([PidLidTaskLastUpdate](pidlidtasklastupdate-canonical-property.md)) property must also be set to the current time.</span></span> <span data-ttu-id="ec638-118">A tabela a seguir mostra os valores da propriedade **dispidTaskHistory** , listados em ordem de prioridade decrescente.</span><span class="sxs-lookup"><span data-stu-id="ec638-118">The following table shows the **dispidTaskHistory** property values, listed in order of decreasing priority.</span></span> 
  
|<span data-ttu-id="ec638-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ec638-119">**Value**</span></span>|<span data-ttu-id="ec638-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ec638-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec638-121">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ec638-121">0x00000004</span></span>  <br/> |<span data-ttu-id="ec638-122">A propriedade **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) foi alterada.</span><span class="sxs-lookup"><span data-stu-id="ec638-122">The **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) property changed.</span></span>  <br/> |
|<span data-ttu-id="ec638-123">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ec638-123">0x00000003</span></span>  <br/> |<span data-ttu-id="ec638-124">Outra propriedade foi alterada.</span><span class="sxs-lookup"><span data-stu-id="ec638-124">Another property was changed.</span></span>  <br/> |
|<span data-ttu-id="ec638-125">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ec638-125">0x00000001</span></span>  <br/> |<span data-ttu-id="ec638-126">O destinatário da tarefa aceitou essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec638-126">The task assignee accepted this task.</span></span>  <br/> |
|<span data-ttu-id="ec638-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ec638-127">0x00000002</span></span>  <br/> |<span data-ttu-id="ec638-128">O destinatário da tarefa rejeitou essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec638-128">The task assignee rejected this task.</span></span>  <br/> |
|<span data-ttu-id="ec638-129">0x00000005</span><span class="sxs-lookup"><span data-stu-id="ec638-129">0x00000005</span></span>  <br/> |<span data-ttu-id="ec638-130">A tarefa foi atribuída a um destinatário de tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec638-130">The task was assigned to a task assignee.</span></span>  <br/> |
|<span data-ttu-id="ec638-131">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec638-131">0x00000000</span></span>  <br/> |<span data-ttu-id="ec638-132">Nenhuma alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="ec638-132">No changes were made.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ec638-133">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec638-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec638-134">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="ec638-134">Protocol specifications</span></span>

<span data-ttu-id="ec638-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec638-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec638-136">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ec638-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec638-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec638-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec638-138">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ec638-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec638-139">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec638-139">Header files</span></span>

<span data-ttu-id="ec638-140">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ec638-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec638-141">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ec638-141">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec638-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec638-142">See also</span></span>



[<span data-ttu-id="ec638-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec638-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec638-144">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ec638-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec638-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec638-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec638-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ec638-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


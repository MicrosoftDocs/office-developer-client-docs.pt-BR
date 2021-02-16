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
ms.openlocfilehash: d0ae319a6b5fa4c901ec7d318c7ebdd216a2adeb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357936"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="cac20-103">Propriedade canônica PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="cac20-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="cac20-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cac20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cac20-105">Especifica o status da atribuição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cac20-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="cac20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cac20-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="cac20-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="cac20-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="cac20-108">Property set:</span></span>  <br/> |<span data-ttu-id="cac20-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="cac20-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="cac20-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="cac20-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cac20-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="cac20-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="cac20-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="cac20-112">Data type:</span></span>  <br/> |<span data-ttu-id="cac20-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cac20-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cac20-114">Área:</span><span class="sxs-lookup"><span data-stu-id="cac20-114">Area:</span></span>  <br/> |<span data-ttu-id="cac20-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="cac20-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cac20-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cac20-116">Remarks</span></span>

<span data-ttu-id="cac20-117">O valor deve ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="cac20-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="cac20-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cac20-118">**Value**</span></span>|<span data-ttu-id="cac20-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cac20-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cac20-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cac20-120">0x00000000</span></span>  <br/> |<span data-ttu-id="cac20-121">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="cac20-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="cac20-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="cac20-122">0x00000001</span></span>  <br/> |<span data-ttu-id="cac20-123">A tarefa é incorporada em uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="cac20-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="cac20-124">0x00000002</span></span>  <br/> |<span data-ttu-id="cac20-125">A tarefa foi aceita pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="cac20-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="cac20-126">0x00000003</span></span>  <br/> |<span data-ttu-id="cac20-127">A tarefa foi rejeitada pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="cac20-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="cac20-128">0x00000004</span></span>  <br/> |<span data-ttu-id="cac20-129">A tarefa é incorporada em uma atualização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="cac20-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cac20-130">0x00000005</span></span>  <br/> |<span data-ttu-id="cac20-131">A tarefa foi atribuída ao designador da tarefa.</span><span class="sxs-lookup"><span data-stu-id="cac20-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="cac20-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="cac20-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cac20-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="cac20-133">Protocol specifications</span></span>

<span data-ttu-id="cac20-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cac20-134">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cac20-135">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cac20-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cac20-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cac20-136">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cac20-137">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="cac20-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cac20-138">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="cac20-138">Header files</span></span>

<span data-ttu-id="cac20-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cac20-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="cac20-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="cac20-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cac20-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cac20-141">See also</span></span>



[<span data-ttu-id="cac20-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="cac20-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cac20-143">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="cac20-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cac20-144">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="cac20-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cac20-145">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="cac20-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


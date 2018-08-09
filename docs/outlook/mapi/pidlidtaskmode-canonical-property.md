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
ms.openlocfilehash: f8eef7863cec565403d41dae26687b75f078e0d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768725"
---
# <a name="pidlidtaskmode-canonical-property"></a><span data-ttu-id="a7564-103">Propriedade canônica PidLidTaskMode</span><span class="sxs-lookup"><span data-stu-id="a7564-103">PidLidTaskMode Canonical Property</span></span>

  
  
<span data-ttu-id="a7564-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7564-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7564-105">Especifica o status de atribuição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-105">Specifies the assignment status of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7564-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a7564-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7564-107">dispidTaskMode</span><span class="sxs-lookup"><span data-stu-id="a7564-107">dispidTaskMode</span></span>  <br/> |
|<span data-ttu-id="a7564-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="a7564-108">Property set:</span></span>  <br/> |<span data-ttu-id="a7564-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a7564-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a7564-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="a7564-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a7564-111">0x00008518</span><span class="sxs-lookup"><span data-stu-id="a7564-111">0x00008518</span></span>  <br/> |
|<span data-ttu-id="a7564-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a7564-112">Data type:</span></span>  <br/> |<span data-ttu-id="a7564-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a7564-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a7564-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a7564-114">Area:</span></span>  <br/> |<span data-ttu-id="a7564-115">Task</span><span class="sxs-lookup"><span data-stu-id="a7564-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7564-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7564-116">Remarks</span></span>

<span data-ttu-id="a7564-117">O valor deve ser um destes procedimentos.</span><span class="sxs-lookup"><span data-stu-id="a7564-117">The value must be one of the following.</span></span>
  
|<span data-ttu-id="a7564-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a7564-118">**Value**</span></span>|<span data-ttu-id="a7564-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a7564-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7564-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a7564-120">0x00000000</span></span>  <br/> |<span data-ttu-id="a7564-121">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="a7564-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="a7564-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a7564-122">0x00000001</span></span>  <br/> |<span data-ttu-id="a7564-123">A tarefa está incorporada em uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-123">The task is embedded in a task request.</span></span>  <br/> |
|<span data-ttu-id="a7564-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a7564-124">0x00000002</span></span>  <br/> |<span data-ttu-id="a7564-125">A tarefa foi aceita pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-125">The task was accepted by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="a7564-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a7564-126">0x00000003</span></span>  <br/> |<span data-ttu-id="a7564-127">A tarefa foi rejeitada pelo destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-127">The task was rejected by the task assignee.</span></span>  <br/> |
|<span data-ttu-id="a7564-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a7564-128">0x00000004</span></span>  <br/> |<span data-ttu-id="a7564-129">A tarefa está incorporada em uma atualização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-129">The task is embedded in a task update.</span></span>  <br/> |
|<span data-ttu-id="a7564-130">0x00000005</span><span class="sxs-lookup"><span data-stu-id="a7564-130">0x00000005</span></span>  <br/> |<span data-ttu-id="a7564-131">A tarefa foi atribuída ao cedente a tarefa.</span><span class="sxs-lookup"><span data-stu-id="a7564-131">The task was assigned to the task assigner.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a7564-132">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7564-132">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7564-133">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a7564-133">Protocol specifications</span></span>

<span data-ttu-id="a7564-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7564-134">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7564-135">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a7564-135">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7564-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7564-136">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7564-137">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a7564-137">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7564-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a7564-138">Header files</span></span>

<span data-ttu-id="a7564-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7564-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7564-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a7564-140">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7564-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7564-141">See also</span></span>



[<span data-ttu-id="a7564-142">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a7564-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7564-143">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a7564-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7564-144">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7564-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7564-145">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a7564-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


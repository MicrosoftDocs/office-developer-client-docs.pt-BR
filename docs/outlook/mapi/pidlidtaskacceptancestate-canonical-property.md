---
title: Propriedade canônica PidLidTaskAcceptanceState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAcceptanceState
api_type:
- COM
ms.assetid: 7012f524-bc66-48ea-85b5-163e05029d35
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b42be4b42d085aba8999a8c3f1a780ed972fa136
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331287"
---
# <a name="pidlidtaskacceptancestate-canonical-property"></a><span data-ttu-id="b5011-103">Propriedade canônica PidLidTaskAcceptanceState</span><span class="sxs-lookup"><span data-stu-id="b5011-103">PidLidTaskAcceptanceState Canonical Property</span></span>

  
  
<span data-ttu-id="b5011-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5011-105">Indica o estado de aceitação da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5011-105">Indicates the acceptance state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5011-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b5011-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5011-107">dispidTaskDelegValue</span><span class="sxs-lookup"><span data-stu-id="b5011-107">dispidTaskDelegValue</span></span>  <br/> |
|<span data-ttu-id="b5011-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b5011-108">Property set:</span></span>  <br/> |<span data-ttu-id="b5011-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b5011-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b5011-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b5011-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b5011-111">0x0000812A</span><span class="sxs-lookup"><span data-stu-id="b5011-111">0x0000812A</span></span>  <br/> |
|<span data-ttu-id="b5011-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b5011-112">Data type:</span></span>  <br/> |<span data-ttu-id="b5011-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5011-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5011-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b5011-114">Area:</span></span>  <br/> |<span data-ttu-id="b5011-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="b5011-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5011-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5011-116">Remarks</span></span>

<span data-ttu-id="b5011-117">A tabela a seguir mostra os valores possíveis para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b5011-117">The following table shows the possible values for this property.</span></span>
  
|<span data-ttu-id="b5011-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b5011-118">**Value**</span></span>|<span data-ttu-id="b5011-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b5011-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b5011-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b5011-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b5011-121">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="b5011-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="b5011-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b5011-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b5011-123">O status de aceitação da tarefa é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b5011-123">The task's acceptance status is unknown.</span></span>  <br/> |
|<span data-ttu-id="b5011-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b5011-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b5011-125">O destinatário da tarefa aceitou a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5011-125">The task assignee accepted the task.</span></span> <span data-ttu-id="b5011-126">Esse valor é definido quando o cliente processa uma aceitação da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5011-126">This value is set when the client processes a task acceptance.</span></span>  <br/> |
|<span data-ttu-id="b5011-127">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b5011-127">0x00000003</span></span>  <br/> |<span data-ttu-id="b5011-128">O destinatário da tarefa rejeitou a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5011-128">The task assignee rejected the task.</span></span> <span data-ttu-id="b5011-129">Esse valor é definido quando o cliente processa uma rejeição de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5011-129">This value is set when the client processes a task rejection.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b5011-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5011-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5011-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b5011-131">Protocol specifications</span></span>

<span data-ttu-id="b5011-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5011-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5011-133">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b5011-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5011-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5011-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5011-135">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b5011-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5011-136">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b5011-136">Header files</span></span>

<span data-ttu-id="b5011-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5011-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5011-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5011-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5011-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5011-139">See also</span></span>



[<span data-ttu-id="b5011-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5011-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5011-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b5011-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5011-142">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b5011-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5011-143">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b5011-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


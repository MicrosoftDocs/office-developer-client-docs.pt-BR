---
title: Propriedade canônica PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303061"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="abf28-103">Propriedade canônica PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="abf28-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="abf28-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abf28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abf28-105">Contém uma pilha de entradas que representam os atribuídores de tarefa.</span><span class="sxs-lookup"><span data-stu-id="abf28-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="abf28-106">O atribuídor de tarefa mais recente aparece na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="abf28-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abf28-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="abf28-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="abf28-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="abf28-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="abf28-109">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="abf28-109">Property set:</span></span>  <br/> |<span data-ttu-id="abf28-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="abf28-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="abf28-111">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="abf28-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abf28-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="abf28-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="abf28-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="abf28-113">Data type:</span></span>  <br/> |<span data-ttu-id="abf28-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="abf28-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="abf28-115">Área:</span><span class="sxs-lookup"><span data-stu-id="abf28-115">Area:</span></span>  <br/> |<span data-ttu-id="abf28-116">Tarefas</span><span class="sxs-lookup"><span data-stu-id="abf28-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abf28-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="abf28-117">Remarks</span></span>

<span data-ttu-id="abf28-118">Quando o cliente recebe uma solicitação de tarefa, ele anexa a essa propriedade, que estrutura é definida em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), uma entrada que representa o remetente da tarefa.</span><span class="sxs-lookup"><span data-stu-id="abf28-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="abf28-119">Quando o cliente recebe uma rejeição de tarefa, o cliente remove a última entrada do atribuídor de tarefa dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="abf28-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="abf28-120">Quando o cliente envia uma resposta de tarefa, o cliente a envia para o último atribuídor de tarefas listado no valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="abf28-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abf28-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="abf28-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abf28-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="abf28-122">Protocol specifications</span></span>

<span data-ttu-id="abf28-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abf28-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abf28-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="abf28-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abf28-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abf28-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abf28-126">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas</span><span class="sxs-lookup"><span data-stu-id="abf28-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="abf28-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="abf28-127">Header files</span></span>

<span data-ttu-id="abf28-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abf28-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="abf28-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="abf28-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abf28-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="abf28-130">See also</span></span>



[<span data-ttu-id="abf28-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="abf28-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abf28-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="abf28-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abf28-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="abf28-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abf28-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="abf28-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


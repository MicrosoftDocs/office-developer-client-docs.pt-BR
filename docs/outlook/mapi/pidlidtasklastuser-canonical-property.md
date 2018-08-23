---
title: Propriedade canônica PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db94d68a01b65410cf4f3f1f461c780f2bb01918
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568529"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="e90e5-103">Propriedade canônica PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="e90e5-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="e90e5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e90e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e90e5-105">Os nomes de usuário mais recente que foi o proprietário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e90e5-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e90e5-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e90e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e90e5-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="e90e5-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="e90e5-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="e90e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="e90e5-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e90e5-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e90e5-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="e90e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e90e5-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="e90e5-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="e90e5-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e90e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="e90e5-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e90e5-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e90e5-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e90e5-114">Area:</span></span>  <br/> |<span data-ttu-id="e90e5-115">Task</span><span class="sxs-lookup"><span data-stu-id="e90e5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e90e5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e90e5-116">Remarks</span></span>

<span data-ttu-id="e90e5-117">Antes de um cliente envia uma solicitação de tarefa, ele define essa propriedade com o nome da cedente a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e90e5-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="e90e5-118">Antes de um cliente envia a aceitação de uma tarefa, ela define essa propriedade como o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e90e5-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="e90e5-119">Antes de um cliente envia uma rejeição da tarefa, ele define essa propriedade com o nome da cedente a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e90e5-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e90e5-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e90e5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e90e5-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e90e5-121">Protocol specifications</span></span>

<span data-ttu-id="e90e5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e90e5-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e90e5-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e90e5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e90e5-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e90e5-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e90e5-125">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="e90e5-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e90e5-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e90e5-126">Header files</span></span>

<span data-ttu-id="e90e5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e90e5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="e90e5-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e90e5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e90e5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e90e5-129">See also</span></span>



[<span data-ttu-id="e90e5-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e90e5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e90e5-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e90e5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e90e5-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e90e5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e90e5-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e90e5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


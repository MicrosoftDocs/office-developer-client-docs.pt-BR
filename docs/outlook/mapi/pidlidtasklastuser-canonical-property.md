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
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360442"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="07d48-103">Propriedade canônica PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="07d48-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="07d48-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07d48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07d48-105">Nomeia o usuário mais recente que era o proprietário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="07d48-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="07d48-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="07d48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07d48-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="07d48-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="07d48-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="07d48-108">Property set:</span></span>  <br/> |<span data-ttu-id="07d48-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="07d48-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="07d48-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="07d48-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="07d48-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="07d48-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="07d48-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="07d48-112">Data type:</span></span>  <br/> |<span data-ttu-id="07d48-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="07d48-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="07d48-114">Área:</span><span class="sxs-lookup"><span data-stu-id="07d48-114">Area:</span></span>  <br/> |<span data-ttu-id="07d48-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="07d48-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07d48-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="07d48-116">Remarks</span></span>

<span data-ttu-id="07d48-117">Antes de um cliente enviar uma solicitação de tarefa, ele define essa propriedade com o nome do atribuídor de tarefa.</span><span class="sxs-lookup"><span data-stu-id="07d48-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="07d48-118">Antes de um cliente enviar uma aceitação da tarefa, ele define essa propriedade como o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="07d48-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="07d48-119">Antes de um cliente enviar uma rejeição de tarefa, ele define essa propriedade com o nome do atribuídor de tarefa.</span><span class="sxs-lookup"><span data-stu-id="07d48-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="07d48-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07d48-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07d48-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="07d48-121">Protocol specifications</span></span>

<span data-ttu-id="07d48-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07d48-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07d48-123">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="07d48-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07d48-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07d48-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07d48-125">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="07d48-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07d48-126">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="07d48-126">Header files</span></span>

<span data-ttu-id="07d48-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07d48-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="07d48-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="07d48-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07d48-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="07d48-129">See also</span></span>



[<span data-ttu-id="07d48-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07d48-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07d48-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="07d48-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07d48-132">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="07d48-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07d48-133">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="07d48-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidLidTaskDueDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDueDate
api_type:
- COM
ms.assetid: 69ed3d48-3741-4a9a-8f98-51382b850c27
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e21d164cbb9403d3fa1dc05cf474359a517d64b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303322"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="1ccad-103">Propriedade canônica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="1ccad-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="1ccad-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ccad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ccad-105">Representa a data em que o usuário espera concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="1ccad-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1ccad-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1ccad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ccad-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="1ccad-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="1ccad-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="1ccad-108">Property set:</span></span>  <br/> |<span data-ttu-id="1ccad-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="1ccad-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="1ccad-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1ccad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1ccad-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="1ccad-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="1ccad-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1ccad-112">Data type:</span></span>  <br/> |<span data-ttu-id="1ccad-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1ccad-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1ccad-114">Área:</span><span class="sxs-lookup"><span data-stu-id="1ccad-114">Area:</span></span>  <br/> |<span data-ttu-id="1ccad-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="1ccad-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ccad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ccad-116">Remarks</span></span>

<span data-ttu-id="1ccad-117">A tarefa não terá data de vencimento se essa propriedade não for definida ou definida como 0x5AE980E0 (1.525.252.320).</span><span class="sxs-lookup"><span data-stu-id="1ccad-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="1ccad-118">No entanto, uma data de vencimento será opcional somente se nenhuma data de início for indicada na **propriedade dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1ccad-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="1ccad-119">Se a tarefa tiver uma data de vencimento, o valor deverá ter um componente de hora da meia-noite e a propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="1ccad-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="1ccad-120">Se **dispidTaskStartDate** tiver uma data de início, o valor da propriedade **dispidTaskDueDate** deve ser maior ou igual ao valor de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="1ccad-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1ccad-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ccad-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ccad-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1ccad-122">Protocol specifications</span></span>

<span data-ttu-id="1ccad-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ccad-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ccad-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1ccad-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ccad-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ccad-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ccad-126">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="1ccad-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="1ccad-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ccad-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ccad-128">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="1ccad-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ccad-129">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1ccad-129">Header files</span></span>

<span data-ttu-id="1ccad-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ccad-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ccad-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1ccad-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ccad-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ccad-132">See also</span></span>



[<span data-ttu-id="1ccad-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1ccad-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ccad-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ccad-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ccad-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1ccad-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ccad-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1ccad-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


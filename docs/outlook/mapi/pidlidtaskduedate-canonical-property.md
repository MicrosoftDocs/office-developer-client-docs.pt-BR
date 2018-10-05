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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391791"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="55c57-103">Propriedade canônica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="55c57-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="55c57-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55c57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55c57-105">Representa a data quando o usuário espera para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="55c57-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55c57-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="55c57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55c57-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="55c57-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="55c57-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="55c57-108">Property set:</span></span>  <br/> |<span data-ttu-id="55c57-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="55c57-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="55c57-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="55c57-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55c57-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="55c57-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="55c57-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="55c57-112">Data type:</span></span>  <br/> |<span data-ttu-id="55c57-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="55c57-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="55c57-114">Área:</span><span class="sxs-lookup"><span data-stu-id="55c57-114">Area:</span></span>  <br/> |<span data-ttu-id="55c57-115">Task</span><span class="sxs-lookup"><span data-stu-id="55c57-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c57-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c57-116">Remarks</span></span>

<span data-ttu-id="55c57-117">A tarefa tem sem data de conclusão se essa propriedade for não definidas ou está definida para 0x5AE980E0 (1,525,252,320).</span><span class="sxs-lookup"><span data-stu-id="55c57-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="55c57-118">No entanto, uma data de vencimento é opcional apenas se nenhuma data de início é indicada na propriedade **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="55c57-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="55c57-119">Se a tarefa tiver uma data de vencimento, o valor deve ter um componente de hora de meia-noite e a propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) também deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="55c57-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="55c57-120">Se **dispidTaskStartDate** tiver uma data de início, o valor da propriedade **dispidTaskDueDate** deve ser maior ou igual ao valor de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="55c57-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55c57-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="55c57-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55c57-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="55c57-122">Protocol specifications</span></span>

<span data-ttu-id="55c57-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c57-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c57-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="55c57-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55c57-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c57-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c57-126">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="55c57-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="55c57-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55c57-127">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55c57-128">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="55c57-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55c57-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="55c57-129">Header files</span></span>

<span data-ttu-id="55c57-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55c57-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="55c57-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="55c57-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55c57-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c57-132">See also</span></span>



[<span data-ttu-id="55c57-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="55c57-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55c57-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="55c57-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55c57-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="55c57-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55c57-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="55c57-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


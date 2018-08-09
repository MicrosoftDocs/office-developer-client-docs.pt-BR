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
ms.openlocfilehash: d26a686573a9dc178a46b7dfdc5c18485303b7ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768709"
---
# <a name="pidlidtaskduedate-canonical-property"></a><span data-ttu-id="b5479-103">Propriedade canônica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="b5479-103">PidLidTaskDueDate Canonical Property</span></span>

  
  
<span data-ttu-id="b5479-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5479-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5479-105">Representa a data quando o usuário espera para concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b5479-105">Represents the date when the user expects to complete the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5479-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b5479-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5479-107">dispidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="b5479-107">dispidTaskDueDate</span></span>  <br/> |
|<span data-ttu-id="b5479-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="b5479-108">Property set:</span></span>  <br/> |<span data-ttu-id="b5479-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b5479-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b5479-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="b5479-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b5479-111">0x00008105</span><span class="sxs-lookup"><span data-stu-id="b5479-111">0x00008105</span></span>  <br/> |
|<span data-ttu-id="b5479-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b5479-112">Data type:</span></span>  <br/> |<span data-ttu-id="b5479-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b5479-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b5479-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b5479-114">Area:</span></span>  <br/> |<span data-ttu-id="b5479-115">Task</span><span class="sxs-lookup"><span data-stu-id="b5479-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5479-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5479-116">Remarks</span></span>

<span data-ttu-id="b5479-117">A tarefa tem sem data de conclusão se essa propriedade for não definidas ou está definida para 0x5AE980E0 (1,525,252,320).</span><span class="sxs-lookup"><span data-stu-id="b5479-117">The task has no due date if this property is unset or set to 0x5AE980E0 (1,525,252,320).</span></span> <span data-ttu-id="b5479-118">No entanto, uma data de vencimento é opcional apenas se nenhuma data de início é indicada na propriedade **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b5479-118">However, a due date is optional only if no start date is indicated in the **dispidTaskStartDate** ([PidLidTaskStartDate](pidlidtaskstartdate-canonical-property.md)) property.</span></span> <span data-ttu-id="b5479-119">Se a tarefa tiver uma data de vencimento, o valor deve ter um componente de hora de meia-noite e a propriedade **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) também deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="b5479-119">If the task has a due date, the value must have a time component of midnight, and the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property must also be set.</span></span> <span data-ttu-id="b5479-120">Se **dispidTaskStartDate** tiver uma data de início, o valor da propriedade **dispidTaskDueDate** deve ser maior ou igual ao valor de **dispidTaskStartDate**.</span><span class="sxs-lookup"><span data-stu-id="b5479-120">If **dispidTaskStartDate** has a start date, then the value of the **dispidTaskDueDate** property must be greater than or equal to the value of **dispidTaskStartDate**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5479-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5479-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5479-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b5479-122">Protocol specifications</span></span>

<span data-ttu-id="b5479-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5479-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5479-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b5479-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5479-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5479-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5479-126">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="b5479-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="b5479-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5479-127">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5479-128">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="b5479-128">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5479-129">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5479-129">Header files</span></span>

<span data-ttu-id="b5479-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5479-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5479-131">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b5479-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5479-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5479-132">See also</span></span>



[<span data-ttu-id="b5479-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b5479-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5479-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b5479-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5479-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b5479-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5479-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b5479-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


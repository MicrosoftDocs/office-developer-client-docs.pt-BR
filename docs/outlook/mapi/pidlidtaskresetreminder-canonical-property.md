---
title: Propriedade canônica PidLidTaskResetReminder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskResetReminder
api_type:
- COM
ms.assetid: f6da69ff-a913-4a65-bb07-8ad3c5685e5e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a438fb2b1862d44905a63fda3e5f68b7878cd99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316615"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="ec27f-103">Propriedade canônica PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="ec27f-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="ec27f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec27f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec27f-105">Indica se instâncias futuras de tarefas recorrentes precisam de lembretes, mesmo que **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) seja FALSO.</span><span class="sxs-lookup"><span data-stu-id="ec27f-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec27f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ec27f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ec27f-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="ec27f-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="ec27f-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="ec27f-108">Property set:</span></span>  <br/> |<span data-ttu-id="ec27f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="ec27f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="ec27f-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="ec27f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ec27f-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="ec27f-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="ec27f-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ec27f-112">Data type:</span></span>  <br/> |<span data-ttu-id="ec27f-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ec27f-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ec27f-114">Área:</span><span class="sxs-lookup"><span data-stu-id="ec27f-114">Area:</span></span>  <br/> |<span data-ttu-id="ec27f-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="ec27f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec27f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec27f-116">Remarks</span></span>

<span data-ttu-id="ec27f-117">Esse valor é definido como TRUE quando o lembrete da tarefa é ignorado e definido como FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ec27f-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="ec27f-118">Se não for desa soterado, será assumido o padrão FALSE.</span><span class="sxs-lookup"><span data-stu-id="ec27f-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="ec27f-119">Conforme especificado em [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), a **propriedade dispidReminderSet** indica se um lembrete está definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec27f-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="ec27f-120">No entanto, essa propriedade só indica a presença de um lembrete em uma única tarefa.</span><span class="sxs-lookup"><span data-stu-id="ec27f-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="ec27f-121">Ele não pode ser usado sozinho para determinar se uma instância futura de uma tarefa recorrente precisa de um lembrete.</span><span class="sxs-lookup"><span data-stu-id="ec27f-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ec27f-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ec27f-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ec27f-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ec27f-123">Protocol specifications</span></span>

<span data-ttu-id="ec27f-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec27f-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec27f-125">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ec27f-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ec27f-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec27f-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec27f-127">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="ec27f-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="ec27f-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec27f-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ec27f-129">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="ec27f-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ec27f-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="ec27f-130">Header files</span></span>

<span data-ttu-id="ec27f-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ec27f-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ec27f-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ec27f-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec27f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec27f-133">See also</span></span>



[<span data-ttu-id="ec27f-134">Propriedade can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="ec27f-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="ec27f-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ec27f-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ec27f-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="ec27f-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ec27f-137">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec27f-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ec27f-138">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ec27f-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


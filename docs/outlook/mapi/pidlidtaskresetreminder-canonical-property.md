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
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="71888-103">Propriedade canônica PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="71888-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="71888-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71888-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71888-105">Indica se futuras instâncias de tarefas recorrentes precisam de lembretes, mesmo que **dispidReminderSet** ([PIDLIDREMINDERSET](pidlidreminderset-canonical-property.md)) seja falso.</span><span class="sxs-lookup"><span data-stu-id="71888-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71888-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="71888-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="71888-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="71888-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="71888-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="71888-108">Property set:</span></span>  <br/> |<span data-ttu-id="71888-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="71888-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="71888-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="71888-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="71888-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="71888-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="71888-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="71888-112">Data type:</span></span>  <br/> |<span data-ttu-id="71888-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="71888-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="71888-114">Área:</span><span class="sxs-lookup"><span data-stu-id="71888-114">Area:</span></span>  <br/> |<span data-ttu-id="71888-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="71888-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71888-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="71888-116">Remarks</span></span>

<span data-ttu-id="71888-117">Esse valor é definido como TRUE quando o lembrete da tarefa é ignorado e, caso contrário, é definido como FALSE.</span><span class="sxs-lookup"><span data-stu-id="71888-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="71888-118">Se a redefinição à esquerda, um padrão FALSE será adotado.</span><span class="sxs-lookup"><span data-stu-id="71888-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="71888-119">Conforme especificado em [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), a propriedade **dispidReminderSet** indica se um lembrete está definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="71888-119">As specified in [[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="71888-120">No enTanto, essa propriedade indica apenas a presença de um lembrete em uma única tarefa.</span><span class="sxs-lookup"><span data-stu-id="71888-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="71888-121">Ele não pode ser usado sozinho para determinar se uma instância futura de uma tarefa recorrente precisa de um lembrete.</span><span class="sxs-lookup"><span data-stu-id="71888-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="71888-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="71888-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="71888-123">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="71888-123">Protocol specifications</span></span>

<span data-ttu-id="71888-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71888-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71888-125">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="71888-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="71888-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71888-126">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71888-127">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="71888-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="71888-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="71888-128">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="71888-129">Especifica as propriedades e o modelo de interação para email e outros lembretes de objeto.</span><span class="sxs-lookup"><span data-stu-id="71888-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="71888-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="71888-130">Header files</span></span>

<span data-ttu-id="71888-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="71888-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="71888-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="71888-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="71888-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="71888-133">See also</span></span>



[<span data-ttu-id="71888-134">Propriedade can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="71888-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="71888-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="71888-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="71888-136">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="71888-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="71888-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="71888-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="71888-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="71888-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


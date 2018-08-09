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
ms.openlocfilehash: a95fc30de7511672cb27c9dd6fbc37b96e822e77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768732"
---
# <a name="pidlidtaskresetreminder-canonical-property"></a><span data-ttu-id="02439-103">Propriedade canônica PidLidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="02439-103">PidLidTaskResetReminder Canonical Property</span></span>

  
  
<span data-ttu-id="02439-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="02439-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="02439-105">Indica se a instâncias futuras do tarefas recorrentes precisam lembretes, embora **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) é FALSE.</span><span class="sxs-lookup"><span data-stu-id="02439-105">Indicates whether future instances of recurring tasks need reminders, even though **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) is FALSE.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02439-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="02439-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02439-107">dispidTaskResetReminder</span><span class="sxs-lookup"><span data-stu-id="02439-107">dispidTaskResetReminder</span></span>  <br/> |
|<span data-ttu-id="02439-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="02439-108">Property set:</span></span>  <br/> |<span data-ttu-id="02439-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="02439-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="02439-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="02439-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="02439-111">0x00008107</span><span class="sxs-lookup"><span data-stu-id="02439-111">0x00008107</span></span>  <br/> |
|<span data-ttu-id="02439-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="02439-112">Data type:</span></span>  <br/> |<span data-ttu-id="02439-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="02439-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="02439-114">Área:</span><span class="sxs-lookup"><span data-stu-id="02439-114">Area:</span></span>  <br/> |<span data-ttu-id="02439-115">Task</span><span class="sxs-lookup"><span data-stu-id="02439-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02439-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="02439-116">Remarks</span></span>

<span data-ttu-id="02439-117">Este valor é definido como TRUE quando o lembrete da tarefa é descartado pelo e definida como FALSE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="02439-117">This value is set to TRUE when the task's reminder is dismissed, and set to FALSE otherwise.</span></span> <span data-ttu-id="02439-118">Se for deixado não definidas, um padrão de falso é assumido.</span><span class="sxs-lookup"><span data-stu-id="02439-118">If left unset, a default of FALSE is assumed.</span></span>
  
<span data-ttu-id="02439-119">Conforme especificado na [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), a propriedade **dispidReminderSet** indica se um lembrete está definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="02439-119">As specified in [[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx), the **dispidReminderSet** property indicates whether a reminder is set on the task.</span></span> <span data-ttu-id="02439-120">No entanto, essa propriedade somente indica a presença de um lembrete em uma única tarefa.</span><span class="sxs-lookup"><span data-stu-id="02439-120">However, this property only indicates the presence of a reminder on a single task.</span></span> <span data-ttu-id="02439-121">Ele não pode ser usado sozinho para determinar se uma instância futura de uma tarefa recorrente precisa de um lembrete.</span><span class="sxs-lookup"><span data-stu-id="02439-121">It cannot be used alone to determine whether a future instance of a recurring task needs a reminder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02439-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="02439-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02439-123">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="02439-123">Protocol specifications</span></span>

<span data-ttu-id="02439-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02439-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02439-125">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="02439-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02439-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02439-126">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02439-127">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="02439-127">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="02439-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02439-128">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02439-129">Especifica as propriedades e o modelo de interação para email e lembretes de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="02439-129">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02439-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="02439-130">Header files</span></span>

<span data-ttu-id="02439-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02439-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="02439-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="02439-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02439-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="02439-133">See also</span></span>



[<span data-ttu-id="02439-134">Propriedade can�nico de PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="02439-134">PidLidReminderSet Canonical Property</span></span>](pidlidreminderset-canonical-property.md)


[<span data-ttu-id="02439-135">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="02439-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02439-136">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="02439-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02439-137">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="02439-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02439-138">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="02439-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


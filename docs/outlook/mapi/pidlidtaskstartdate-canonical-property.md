---
title: Propriedade canônica PidLidTaskStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStartDate
api_type:
- COM
ms.assetid: fe87eb3d-21d1-45bb-b848-e141ce1be6a0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b17a5791db4ccb840224785dd71a2ed52143cbaf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565442"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="72fe0-103">Propriedade canônica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="72fe0-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="72fe0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72fe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72fe0-105">A data quando o usuário espera para começar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="72fe0-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72fe0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="72fe0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72fe0-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="72fe0-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="72fe0-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="72fe0-108">Property set:</span></span>  <br/> |<span data-ttu-id="72fe0-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="72fe0-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="72fe0-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="72fe0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="72fe0-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="72fe0-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="72fe0-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="72fe0-112">Data type:</span></span>  <br/> |<span data-ttu-id="72fe0-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="72fe0-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="72fe0-114">Área:</span><span class="sxs-lookup"><span data-stu-id="72fe0-114">Area:</span></span>  <br/> |<span data-ttu-id="72fe0-115">Task</span><span class="sxs-lookup"><span data-stu-id="72fe0-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72fe0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="72fe0-116">Remarks</span></span>

<span data-ttu-id="72fe0-117">Se o valor dessa propriedade for deixado não definida, a tarefa não tem uma data de início.</span><span class="sxs-lookup"><span data-stu-id="72fe0-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="72fe0-118">Um valor igual a "0x5AE980E0" (1,525,252,320) também significa que a tarefa não possui uma data de início.</span><span class="sxs-lookup"><span data-stu-id="72fe0-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="72fe0-119">Se a tarefa tiver uma data de início, o valor deve ter um componente de hora de meia-noite e as propriedades de **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) e o **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) também devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="72fe0-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="72fe0-120">Essa propriedade é compartilhada pela especificação do protocolo de sinalização informativos e especificação de protocolo do objeto Task-Related localizados em [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="72fe0-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72fe0-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="72fe0-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72fe0-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="72fe0-122">Protocol specifications</span></span>

<span data-ttu-id="72fe0-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72fe0-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72fe0-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="72fe0-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72fe0-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72fe0-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72fe0-126">Especifica as propriedades e operações que são permitidas em contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="72fe0-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72fe0-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="72fe0-127">Header files</span></span>

<span data-ttu-id="72fe0-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72fe0-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="72fe0-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="72fe0-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72fe0-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="72fe0-130">See also</span></span>



[<span data-ttu-id="72fe0-131">Propriedade can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="72fe0-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="72fe0-132">Propriedade can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="72fe0-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="72fe0-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="72fe0-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72fe0-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="72fe0-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72fe0-135">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="72fe0-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72fe0-136">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="72fe0-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


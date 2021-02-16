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
ms.openlocfilehash: 3bc475292e47a9ad8dd9565e17640ef95e7b3c76
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316678"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="b202d-103">Propriedade canônica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="b202d-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="b202d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b202d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b202d-105">A data em que o usuário espera iniciar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="b202d-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b202d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b202d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b202d-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="b202d-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="b202d-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="b202d-108">Property set:</span></span>  <br/> |<span data-ttu-id="b202d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b202d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b202d-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b202d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b202d-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="b202d-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="b202d-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b202d-112">Data type:</span></span>  <br/> |<span data-ttu-id="b202d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b202d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b202d-114">Área:</span><span class="sxs-lookup"><span data-stu-id="b202d-114">Area:</span></span>  <br/> |<span data-ttu-id="b202d-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="b202d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b202d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b202d-116">Remarks</span></span>

<span data-ttu-id="b202d-117">Se esse valor de propriedade for deixado desa definida, a tarefa não terá uma data de início.</span><span class="sxs-lookup"><span data-stu-id="b202d-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="b202d-118">Um valor "0x5AE980E0" (1.525.252.320) também significa que a tarefa não tem uma data de início.</span><span class="sxs-lookup"><span data-stu-id="b202d-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="b202d-119">Se a tarefa tiver uma data de início, o valor deverá ter um componente de hora da meia-noite, e as propriedades **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) e **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) também deverão ser definidas.</span><span class="sxs-lookup"><span data-stu-id="b202d-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="b202d-120">Essa propriedade é compartilhada pela Especificação do Protocolo de Sinalização Task-Related Informações e especificação de Protocolo de Objeto Task-Related localizada em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b202d-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b202d-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b202d-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b202d-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b202d-122">Protocol specifications</span></span>

<span data-ttu-id="b202d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b202d-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b202d-124">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b202d-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b202d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b202d-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b202d-126">Especifica as propriedades e operações permitidas em contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="b202d-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b202d-127">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b202d-127">Header files</span></span>

<span data-ttu-id="b202d-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b202d-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b202d-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b202d-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b202d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b202d-130">See also</span></span>



[<span data-ttu-id="b202d-131">Propriedade can�nico de PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="b202d-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="b202d-132">Propriedade can�nico de PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="b202d-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="b202d-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b202d-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b202d-134">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b202d-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b202d-135">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b202d-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b202d-136">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b202d-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


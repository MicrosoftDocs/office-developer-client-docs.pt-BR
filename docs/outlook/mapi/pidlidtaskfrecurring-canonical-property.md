---
title: Propriedade canônica PidLidTaskFRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFRecurring
api_type:
- COM
ms.assetid: 47c9ccbb-161c-4829-8ffb-201f3b54cd45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aec9dd328e802e185c870d3ecd94cbd1d10ac67d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303049"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="abe84-103">Propriedade canônica PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="abe84-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="abe84-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abe84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abe84-105">Indica se a tarefa inclui um padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="abe84-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abe84-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="abe84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="abe84-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="abe84-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="abe84-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="abe84-108">Property set:</span></span>  <br/> |<span data-ttu-id="abe84-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="abe84-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="abe84-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="abe84-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="abe84-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="abe84-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="abe84-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="abe84-112">Data type:</span></span>  <br/> |<span data-ttu-id="abe84-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="abe84-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="abe84-114">Área:</span><span class="sxs-lookup"><span data-stu-id="abe84-114">Area:</span></span>  <br/> |<span data-ttu-id="abe84-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="abe84-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="abe84-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="abe84-116">Remarks</span></span>

<span data-ttu-id="abe84-117">Se essa propriedade for deixada sem definição, será assumido o valor padrão FALSE.</span><span class="sxs-lookup"><span data-stu-id="abe84-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="abe84-118">Se for definido como TRUE, as propriedades **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) e **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) também deverão ser definidas como especificado em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="abe84-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="abe84-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="abe84-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="abe84-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="abe84-120">Protocol specifications</span></span>

<span data-ttu-id="abe84-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abe84-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abe84-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="abe84-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="abe84-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="abe84-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="abe84-124">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="abe84-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="abe84-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="abe84-125">Header files</span></span>

<span data-ttu-id="abe84-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="abe84-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="abe84-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="abe84-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="abe84-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="abe84-128">See also</span></span>



[<span data-ttu-id="abe84-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="abe84-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="abe84-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="abe84-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="abe84-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="abe84-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="abe84-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="abe84-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


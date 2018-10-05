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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394451"
---
# <a name="pidlidtaskfrecurring-canonical-property"></a><span data-ttu-id="64df8-103">Propriedade canônica PidLidTaskFRecurring</span><span class="sxs-lookup"><span data-stu-id="64df8-103">PidLidTaskFRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="64df8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64df8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64df8-105">Indica se a tarefa inclui um padrão de recorrência.</span><span class="sxs-lookup"><span data-stu-id="64df8-105">Indicates whether the task includes a recurrence pattern.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64df8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="64df8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="64df8-107">dispidTaskFRecur</span><span class="sxs-lookup"><span data-stu-id="64df8-107">dispidTaskFRecur</span></span>  <br/> |
|<span data-ttu-id="64df8-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="64df8-108">Property set:</span></span>  <br/> |<span data-ttu-id="64df8-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="64df8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="64df8-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="64df8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="64df8-111">0x00008126</span><span class="sxs-lookup"><span data-stu-id="64df8-111">0x00008126</span></span>  <br/> |
|<span data-ttu-id="64df8-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="64df8-112">Data type:</span></span>  <br/> |<span data-ttu-id="64df8-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="64df8-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="64df8-114">Área:</span><span class="sxs-lookup"><span data-stu-id="64df8-114">Area:</span></span>  <br/> |<span data-ttu-id="64df8-115">Task</span><span class="sxs-lookup"><span data-stu-id="64df8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64df8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="64df8-116">Remarks</span></span>

<span data-ttu-id="64df8-117">Se essa propriedade for deixada não definida, um valor padrão FALSE é assumido.</span><span class="sxs-lookup"><span data-stu-id="64df8-117">If this property is left unset, a default value of FALSE is assumed.</span></span> <span data-ttu-id="64df8-118">Se ele for definido como TRUE, o **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) e propriedades de **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) também devem ser definidas como especificado em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="64df8-118">If it is set to TRUE, the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) and **dispidTaskDeadOccur** ([PidLidTaskDeadOccurrence](pidlidtaskdeadoccurrence-canonical-property.md)) properties must also be set as specified in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="64df8-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="64df8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="64df8-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="64df8-120">Protocol specifications</span></span>

<span data-ttu-id="64df8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64df8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64df8-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="64df8-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="64df8-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="64df8-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="64df8-124">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="64df8-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="64df8-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="64df8-125">Header files</span></span>

<span data-ttu-id="64df8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64df8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="64df8-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="64df8-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64df8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="64df8-128">See also</span></span>



[<span data-ttu-id="64df8-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="64df8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="64df8-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="64df8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="64df8-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="64df8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="64df8-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="64df8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


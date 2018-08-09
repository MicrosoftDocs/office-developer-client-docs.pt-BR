---
title: Propriedade canônica PidLidTaskDeadOccurrence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDeadOccurrence
api_type:
- COM
ms.assetid: e78287ff-f8cc-45ea-8da8-e7a7359e651c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 14207e513e935a296ff9b953b92ab1ab9ab41fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768683"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="4e8b4-103">Propriedade canônica PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="4e8b4-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="4e8b4-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4e8b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4e8b4-105">Indica se as novas ocorrências devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e8b4-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4e8b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e8b4-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="4e8b4-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="4e8b4-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="4e8b4-108">Property set:</span></span>  <br/> |<span data-ttu-id="4e8b4-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4e8b4-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4e8b4-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="4e8b4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4e8b4-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="4e8b4-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="4e8b4-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4e8b4-112">Data type:</span></span>  <br/> |<span data-ttu-id="4e8b4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4e8b4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4e8b4-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4e8b4-114">Area:</span></span>  <br/> |<span data-ttu-id="4e8b4-115">Task</span><span class="sxs-lookup"><span data-stu-id="4e8b4-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e8b4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e8b4-116">Remarks</span></span>

<span data-ttu-id="4e8b4-117">Um padrão de recorrência não está mais em vigor quando sua instância final está no passado ou seu número de instâncias especificado foi gerado.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="4e8b4-118">O cliente faz essa propriedade como FALSE para uma nova tarefa ou como TRUE quando ele gera a última instância de uma tarefa recorrente.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="4e8b4-119">Quando você copia uma tarefa para gerar uma nova instância, essa propriedade é definida como TRUE na cópia, que é a instância concluída.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4e8b4-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e8b4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4e8b4-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4e8b4-121">Protocol specifications</span></span>

<span data-ttu-id="4e8b4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b4-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b4-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4e8b4-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4e8b4-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4e8b4-125">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="4e8b4-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e8b4-126">Header files</span></span>

<span data-ttu-id="4e8b4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e8b4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e8b4-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4e8b4-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e8b4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e8b4-129">See also</span></span>



[<span data-ttu-id="4e8b4-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4e8b4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e8b4-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4e8b4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e8b4-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4e8b4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e8b4-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4e8b4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


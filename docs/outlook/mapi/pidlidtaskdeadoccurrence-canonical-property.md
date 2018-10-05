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
ms.openlocfilehash: 0b740368aae43549e81cf3f4f6de40526c505b6b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401507"
---
# <a name="pidlidtaskdeadoccurrence-canonical-property"></a><span data-ttu-id="28be1-103">Propriedade canônica PidLidTaskDeadOccurrence</span><span class="sxs-lookup"><span data-stu-id="28be1-103">PidLidTaskDeadOccurrence Canonical Property</span></span>

  
  
<span data-ttu-id="28be1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28be1-105">Indica se as novas ocorrências devem ser geradas.</span><span class="sxs-lookup"><span data-stu-id="28be1-105">Indicates whether new occurrences must be generated.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="28be1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="28be1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28be1-107">dispidTaskDeadOccur</span><span class="sxs-lookup"><span data-stu-id="28be1-107">dispidTaskDeadOccur</span></span>  <br/> |
|<span data-ttu-id="28be1-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="28be1-108">Property set:</span></span>  <br/> |<span data-ttu-id="28be1-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="28be1-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="28be1-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="28be1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="28be1-111">0x00008109</span><span class="sxs-lookup"><span data-stu-id="28be1-111">0x00008109</span></span>  <br/> |
|<span data-ttu-id="28be1-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="28be1-112">Data type:</span></span>  <br/> |<span data-ttu-id="28be1-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="28be1-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="28be1-114">Área:</span><span class="sxs-lookup"><span data-stu-id="28be1-114">Area:</span></span>  <br/> |<span data-ttu-id="28be1-115">Task</span><span class="sxs-lookup"><span data-stu-id="28be1-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28be1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="28be1-116">Remarks</span></span>

<span data-ttu-id="28be1-117">Um padrão de recorrência não está mais em vigor quando sua instância final está no passado ou seu número de instâncias especificado foi gerado.</span><span class="sxs-lookup"><span data-stu-id="28be1-117">A recurrence pattern is no longer in effect when its final instance is in the past or its specified number of instances has been generated.</span></span> <span data-ttu-id="28be1-118">O cliente faz essa propriedade como FALSE para uma nova tarefa ou como TRUE quando ele gera a última instância de uma tarefa recorrente.</span><span class="sxs-lookup"><span data-stu-id="28be1-118">The client sets this property to FALSE for a new task or to TRUE when it generates the last instance of a recurring task.</span></span> <span data-ttu-id="28be1-119">Quando você copia uma tarefa para gerar uma nova instância, essa propriedade é definida como TRUE na cópia, que é a instância concluída.</span><span class="sxs-lookup"><span data-stu-id="28be1-119">When you copy a task to generate a new instance, this property is set to TRUE on the copy, which is the completed instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="28be1-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="28be1-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28be1-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="28be1-121">Protocol specifications</span></span>

<span data-ttu-id="28be1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28be1-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28be1-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="28be1-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="28be1-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28be1-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28be1-125">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="28be1-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="28be1-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28be1-126">Header files</span></span>

<span data-ttu-id="28be1-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28be1-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="28be1-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="28be1-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28be1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="28be1-129">See also</span></span>



[<span data-ttu-id="28be1-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="28be1-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28be1-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="28be1-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28be1-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="28be1-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28be1-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="28be1-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383524"
---
# <a name="pidlidtaskstartdate-canonical-property"></a><span data-ttu-id="4fc12-103">Propriedade canônica PidLidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="4fc12-103">PidLidTaskStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="4fc12-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fc12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fc12-105">A data quando o usuário espera para começar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4fc12-105">The date when the user expects to begin the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4fc12-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4fc12-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4fc12-107">dispidTaskStartDate</span><span class="sxs-lookup"><span data-stu-id="4fc12-107">dispidTaskStartDate</span></span>  <br/> |
|<span data-ttu-id="4fc12-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="4fc12-108">Property set:</span></span>  <br/> |<span data-ttu-id="4fc12-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4fc12-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4fc12-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4fc12-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4fc12-111">0x00008104</span><span class="sxs-lookup"><span data-stu-id="4fc12-111">0x00008104</span></span>  <br/> |
|<span data-ttu-id="4fc12-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4fc12-112">Data type:</span></span>  <br/> |<span data-ttu-id="4fc12-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="4fc12-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="4fc12-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4fc12-114">Area:</span></span>  <br/> |<span data-ttu-id="4fc12-115">Task</span><span class="sxs-lookup"><span data-stu-id="4fc12-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fc12-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fc12-116">Remarks</span></span>

<span data-ttu-id="4fc12-117">Se o valor dessa propriedade for deixado não definida, a tarefa não tem uma data de início.</span><span class="sxs-lookup"><span data-stu-id="4fc12-117">If this property value is left unset, the task does not have a start date.</span></span> <span data-ttu-id="4fc12-118">Um valor igual a "0x5AE980E0" (1,525,252,320) também significa que a tarefa não possui uma data de início.</span><span class="sxs-lookup"><span data-stu-id="4fc12-118">A value of "0x5AE980E0" (1,525,252,320) also means that the task does not have a start date.</span></span> <span data-ttu-id="4fc12-119">Se a tarefa tiver uma data de início, o valor deve ter um componente de hora de meia-noite e as propriedades de **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) e o **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) também devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="4fc12-119">If the task has a start date, the value must have a time component of midnight, and the **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)) and **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) properties must also be set.</span></span>
  
<span data-ttu-id="4fc12-120">Essa propriedade é compartilhada pela especificação do protocolo de sinalização informativos e especificação de protocolo do objeto Task-Related localizados em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4fc12-120">This property is shared by the Informational Flagging Protocol Specification and Task-Related Object Protocol Specification located in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4fc12-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4fc12-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4fc12-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4fc12-122">Protocol specifications</span></span>

<span data-ttu-id="4fc12-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fc12-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fc12-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="4fc12-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4fc12-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4fc12-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4fc12-126">Especifica as propriedades e operações que são permitidas em contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="4fc12-126">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4fc12-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4fc12-127">Header files</span></span>

<span data-ttu-id="4fc12-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4fc12-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="4fc12-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4fc12-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4fc12-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4fc12-130">See also</span></span>



[<span data-ttu-id="4fc12-131">Propriedade canônica PidLidTaskDueDate</span><span class="sxs-lookup"><span data-stu-id="4fc12-131">PidLidTaskDueDate Canonical Property</span></span>](pidlidtaskduedate-canonical-property.md)
  
[<span data-ttu-id="4fc12-132">Propriedade canônica PidLidCommonStart</span><span class="sxs-lookup"><span data-stu-id="4fc12-132">PidLidCommonStart Canonical Property</span></span>](pidlidcommonstart-canonical-property.md)


[<span data-ttu-id="4fc12-133">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc12-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4fc12-134">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="4fc12-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4fc12-135">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4fc12-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4fc12-136">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="4fc12-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


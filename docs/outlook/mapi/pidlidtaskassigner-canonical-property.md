---
title: Propriedade canônica PidLidTaskAssigner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigner
api_type:
- COM
ms.assetid: f7047e4e-0fb3-476b-9568-8f1135e6d970
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5b711b1e0db0fab93016d3f1c979d81a142c9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768687"
---
# <a name="pidlidtaskassigner-canonical-property"></a><span data-ttu-id="f52de-103">Propriedade canônica PidLidTaskAssigner</span><span class="sxs-lookup"><span data-stu-id="f52de-103">PidLidTaskAssigner Canonical Property</span></span>

  
  
<span data-ttu-id="f52de-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f52de-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f52de-105">Nomes de usuário que foi a último tarefa atribuída a.</span><span class="sxs-lookup"><span data-stu-id="f52de-105">Names the user who was last assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f52de-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f52de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f52de-107">dispidTaskDelegator</span><span class="sxs-lookup"><span data-stu-id="f52de-107">dispidTaskDelegator</span></span>  <br/> |
|<span data-ttu-id="f52de-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="f52de-108">Property set:</span></span>  <br/> |<span data-ttu-id="f52de-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f52de-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f52de-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="f52de-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f52de-111">0x00008121</span><span class="sxs-lookup"><span data-stu-id="f52de-111">0x00008121</span></span>  <br/> |
|<span data-ttu-id="f52de-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f52de-112">Data type:</span></span>  <br/> |<span data-ttu-id="f52de-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f52de-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f52de-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f52de-114">Area:</span></span>  <br/> |<span data-ttu-id="f52de-115">Task</span><span class="sxs-lookup"><span data-stu-id="f52de-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f52de-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f52de-116">Remarks</span></span>

<span data-ttu-id="f52de-117">Se a tarefa não tiver sido atribuída, essa propriedade é da esquerda não definida.</span><span class="sxs-lookup"><span data-stu-id="f52de-117">If the task has not been assigned, this property is left unset.</span></span> <span data-ttu-id="f52de-118">Porque o cliente define essa propriedade depois que o destinatário da tarefa recebe uma solicitação de tarefa, a propriedade não será definida na cópia do cedente a tarefa da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f52de-118">Because the client sets this property after the task assignee receives a task request, the property will not be set on the task assigner's copy of the task.</span></span> <span data-ttu-id="f52de-119">Quando o cliente adiciona ou remove cedente uma tarefa da lista tarefas cedente na propriedade **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)), a propriedade **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) deve ser definido como o adicionado ou cedente de tarefas removidos.</span><span class="sxs-lookup"><span data-stu-id="f52de-119">When the client adds or removes a task assigner from the task assigner list in the **dispidTaskMyDelegators** ([PidLidTaskAssigners](pidlidtaskassigners-canonical-property.md)) property, the **dispidTaskDelegator** ([PidLidTaskAssigner](pidlidtaskassigner-canonical-property.md)) property must be set to the added or removed task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f52de-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f52de-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f52de-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f52de-121">Protocol specifications</span></span>

<span data-ttu-id="f52de-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f52de-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f52de-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f52de-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f52de-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f52de-124">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f52de-125">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f52de-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f52de-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f52de-126">Header files</span></span>

<span data-ttu-id="f52de-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f52de-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f52de-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f52de-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f52de-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f52de-129">See also</span></span>



[<span data-ttu-id="f52de-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f52de-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f52de-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f52de-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f52de-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f52de-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f52de-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f52de-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


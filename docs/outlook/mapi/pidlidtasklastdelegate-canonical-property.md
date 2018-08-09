---
title: Propriedade canônica PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e1a343486e78daae45ca7315ba4d29d44b688bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768706"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="2d303-103">Propriedade canônica PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="2d303-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="2d303-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d303-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="2d303-105">Os nomes de usuário que mais recentemente atribuído ou foi atribuído a tarefa.</span><span class="sxs-lookup"><span data-stu-id="2d303-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d303-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="2d303-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d303-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="2d303-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="2d303-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="2d303-108">Property set:</span></span>  <br/> |<span data-ttu-id="2d303-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="2d303-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="2d303-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="2d303-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2d303-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="2d303-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="2d303-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="2d303-112">Data type:</span></span>  <br/> |<span data-ttu-id="2d303-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2d303-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2d303-114">Área:</span><span class="sxs-lookup"><span data-stu-id="2d303-114">Area:</span></span>  <br/> |<span data-ttu-id="2d303-115">Task</span><span class="sxs-lookup"><span data-stu-id="2d303-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d303-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d303-116">Remarks</span></span>

<span data-ttu-id="2d303-117">Antes de enviar uma solicitação de tarefa, o cliente faz essa propriedade com o nome da cedente a tarefa.</span><span class="sxs-lookup"><span data-stu-id="2d303-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="2d303-118">Antes de enviar uma resposta de tarefa, o cliente faz essa propriedade com o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2d303-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2d303-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d303-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d303-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="2d303-120">Protocol specifications</span></span>

<span data-ttu-id="2d303-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d303-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d303-122">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2d303-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d303-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d303-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d303-124">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="2d303-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d303-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2d303-125">Header files</span></span>

<span data-ttu-id="2d303-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d303-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d303-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="2d303-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d303-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d303-128">See also</span></span>



[<span data-ttu-id="2d303-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="2d303-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d303-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="2d303-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d303-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="2d303-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d303-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="2d303-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


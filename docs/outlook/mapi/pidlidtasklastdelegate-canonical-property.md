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
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355668"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a><span data-ttu-id="4d01c-103">Propriedade canônica PidLidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="4d01c-103">PidLidTaskLastDelegate Canonical Property</span></span>

  
  
<span data-ttu-id="4d01c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d01c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4d01c-105">Nomeia o usuário que mais recentemente atribuiu ou recebeu a tarefa.</span><span class="sxs-lookup"><span data-stu-id="4d01c-105">Names the user who most recently assigned or was assigned the task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d01c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4d01c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d01c-107">dispidTaskLastDelegate</span><span class="sxs-lookup"><span data-stu-id="4d01c-107">dispidTaskLastDelegate</span></span>  <br/> |
|<span data-ttu-id="4d01c-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="4d01c-108">Property set:</span></span>  <br/> |<span data-ttu-id="4d01c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4d01c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4d01c-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4d01c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4d01c-111">0x00008125</span><span class="sxs-lookup"><span data-stu-id="4d01c-111">0x00008125</span></span>  <br/> |
|<span data-ttu-id="4d01c-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="4d01c-112">Data type:</span></span>  <br/> |<span data-ttu-id="4d01c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d01c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d01c-114">Área:</span><span class="sxs-lookup"><span data-stu-id="4d01c-114">Area:</span></span>  <br/> |<span data-ttu-id="4d01c-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="4d01c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d01c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d01c-116">Remarks</span></span>

<span data-ttu-id="4d01c-117">Antes de enviar uma solicitação de tarefa, o cliente define essa propriedade com o nome do atribuídor de tarefa.</span><span class="sxs-lookup"><span data-stu-id="4d01c-117">Before sending a task request, the client sets this property to the name of the task assigner.</span></span> <span data-ttu-id="4d01c-118">Antes de enviar uma resposta de tarefa, o cliente define essa propriedade como o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="4d01c-118">Before sending a task response, the client sets this property to the name of the task assignee.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d01c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d01c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d01c-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4d01c-120">Protocol specifications</span></span>

<span data-ttu-id="4d01c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d01c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d01c-122">Fornece definição de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4d01c-122">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d01c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d01c-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d01c-124">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4d01c-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d01c-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="4d01c-125">Header files</span></span>

<span data-ttu-id="4d01c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d01c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d01c-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4d01c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d01c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d01c-128">See also</span></span>



[<span data-ttu-id="4d01c-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4d01c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d01c-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4d01c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d01c-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4d01c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d01c-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4d01c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


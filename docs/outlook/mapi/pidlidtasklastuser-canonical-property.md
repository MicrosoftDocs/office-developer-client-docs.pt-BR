---
title: Propriedade canônica PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360442"
---
# <a name="pidlidtasklastuser-canonical-property"></a><span data-ttu-id="bd978-103">Propriedade canônica PidLidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="bd978-103">PidLidTaskLastUser Canonical Property</span></span>

  
  
<span data-ttu-id="bd978-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd978-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd978-105">Nomeia o usuário mais recente que foi o proprietário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd978-105">Names the most recent user who was the task owner.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd978-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bd978-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd978-107">dispidTaskLastUser</span><span class="sxs-lookup"><span data-stu-id="bd978-107">dispidTaskLastUser</span></span>  <br/> |
|<span data-ttu-id="bd978-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="bd978-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd978-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bd978-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bd978-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bd978-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd978-111">0x00008122</span><span class="sxs-lookup"><span data-stu-id="bd978-111">0x00008122</span></span>  <br/> |
|<span data-ttu-id="bd978-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bd978-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd978-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bd978-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bd978-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bd978-114">Area:</span></span>  <br/> |<span data-ttu-id="bd978-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="bd978-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd978-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd978-116">Remarks</span></span>

<span data-ttu-id="bd978-117">Antes de um cliente enviar uma solicitação de tarefa, ele define essa propriedade com o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd978-117">Before a client sends a task request, it sets this property to the name of the task assigner.</span></span> <span data-ttu-id="bd978-118">Antes que um cliente envie uma aceitação de tarefa, ele define essa propriedade com o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd978-118">Before a client sends a task acceptance, it sets this property to the name of the task assignee.</span></span> <span data-ttu-id="bd978-119">Antes que um cliente envie uma rejeição de tarefa, ele define essa propriedade com o nome do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd978-119">Before a client sends a task rejection, it sets this property to the name of the task assigner.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd978-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd978-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd978-121">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="bd978-121">Protocol specifications</span></span>

<span data-ttu-id="bd978-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd978-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd978-123">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="bd978-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd978-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd978-124">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd978-125">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bd978-125">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd978-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bd978-126">Header files</span></span>

<span data-ttu-id="bd978-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bd978-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd978-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd978-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd978-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd978-129">See also</span></span>



[<span data-ttu-id="bd978-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bd978-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd978-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bd978-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd978-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd978-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd978-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bd978-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


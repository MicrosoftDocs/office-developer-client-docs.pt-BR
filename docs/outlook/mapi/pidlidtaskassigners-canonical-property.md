---
title: Propriedade canônica PidLidTaskAssigners
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 20a4cf4fc847bdb361fb73161adeb96afb49e57e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570748"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="6c0da-103">Propriedade canônica PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="6c0da-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="6c0da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c0da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c0da-105">Contém uma pilha de entradas que representam assigners de tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c0da-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="6c0da-106">O mais recente cedente de tarefa é exibida na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="6c0da-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c0da-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6c0da-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c0da-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="6c0da-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="6c0da-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="6c0da-109">Property set:</span></span>  <br/> |<span data-ttu-id="6c0da-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="6c0da-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="6c0da-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="6c0da-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6c0da-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="6c0da-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="6c0da-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6c0da-113">Data type:</span></span>  <br/> |<span data-ttu-id="6c0da-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6c0da-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6c0da-115">Área:</span><span class="sxs-lookup"><span data-stu-id="6c0da-115">Area:</span></span>  <br/> |<span data-ttu-id="6c0da-116">Task</span><span class="sxs-lookup"><span data-stu-id="6c0da-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c0da-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c0da-117">Remarks</span></span>

<span data-ttu-id="6c0da-118">Quando o cliente recebe uma solicitação de tarefa, ele anexa a essa propriedade, qual estrutura é definida em [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), uma entrada que representa o remetente da tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c0da-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="6c0da-119">Quando o cliente recebe uma rejeição da tarefa, o cliente remove a última entrada cedente tarefa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6c0da-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="6c0da-120">Quando o cliente envia uma resposta de tarefa, o cliente envia para o último cedente de tarefa listado no valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="6c0da-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c0da-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c0da-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c0da-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6c0da-122">Protocol specifications</span></span>

<span data-ttu-id="6c0da-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c0da-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c0da-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6c0da-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c0da-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c0da-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c0da-126">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas</span><span class="sxs-lookup"><span data-stu-id="6c0da-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="6c0da-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c0da-127">Header files</span></span>

<span data-ttu-id="6c0da-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c0da-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c0da-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6c0da-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c0da-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c0da-130">See also</span></span>



[<span data-ttu-id="6c0da-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6c0da-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c0da-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6c0da-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c0da-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6c0da-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c0da-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6c0da-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


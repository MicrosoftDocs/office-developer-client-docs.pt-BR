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
ms.openlocfilehash: 97a4915d5422f6c5463ed399835172725b83407f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385071"
---
# <a name="pidlidtaskassigners-canonical-property"></a><span data-ttu-id="b0f67-103">Propriedade canônica PidLidTaskAssigners</span><span class="sxs-lookup"><span data-stu-id="b0f67-103">PidLidTaskAssigners Canonical Property</span></span>

  
  
<span data-ttu-id="b0f67-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0f67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0f67-105">Contém uma pilha de entradas que representam assigners de tarefa.</span><span class="sxs-lookup"><span data-stu-id="b0f67-105">Contains a stack of entries that represent task assigners.</span></span> <span data-ttu-id="b0f67-106">O mais recente cedente de tarefa é exibida na parte superior da pilha.</span><span class="sxs-lookup"><span data-stu-id="b0f67-106">The most recent task assigner appears at the top of the stack.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0f67-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b0f67-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0f67-108">dispidTaskMyDelegators</span><span class="sxs-lookup"><span data-stu-id="b0f67-108">dispidTaskMyDelegators</span></span>  <br/> |
|<span data-ttu-id="b0f67-109">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="b0f67-109">Property set:</span></span>  <br/> |<span data-ttu-id="b0f67-110">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b0f67-110">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b0f67-111">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="b0f67-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b0f67-112">0x00008117</span><span class="sxs-lookup"><span data-stu-id="b0f67-112">0x00008117</span></span>  <br/> |
|<span data-ttu-id="b0f67-113">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b0f67-113">Data type:</span></span>  <br/> |<span data-ttu-id="b0f67-114">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0f67-114">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0f67-115">Área:</span><span class="sxs-lookup"><span data-stu-id="b0f67-115">Area:</span></span>  <br/> |<span data-ttu-id="b0f67-116">Task</span><span class="sxs-lookup"><span data-stu-id="b0f67-116">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0f67-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0f67-117">Remarks</span></span>

<span data-ttu-id="b0f67-118">Quando o cliente recebe uma solicitação de tarefa, ele anexa a essa propriedade, qual estrutura é definida em [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), uma entrada que representa o remetente da tarefa.</span><span class="sxs-lookup"><span data-stu-id="b0f67-118">When the client receives a task request, it appends to this property, which structure is defined in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx), an entry that represents the task's sender.</span></span> <span data-ttu-id="b0f67-119">Quando o cliente recebe uma rejeição da tarefa, o cliente remove a última entrada cedente tarefa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b0f67-119">When the client receives a task rejection, the client removes the last task assigner entry from this property.</span></span> <span data-ttu-id="b0f67-120">Quando o cliente envia uma resposta de tarefa, o cliente envia para o último cedente de tarefa listado no valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b0f67-120">When the client sends a task response, the client sends it to the last task assigner listed in the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0f67-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0f67-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0f67-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="b0f67-122">Protocol specifications</span></span>

<span data-ttu-id="b0f67-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0f67-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0f67-124">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0f67-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0f67-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0f67-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0f67-126">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas</span><span class="sxs-lookup"><span data-stu-id="b0f67-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b0f67-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b0f67-127">Header files</span></span>

<span data-ttu-id="b0f67-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0f67-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0f67-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b0f67-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0f67-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0f67-130">See also</span></span>



[<span data-ttu-id="b0f67-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b0f67-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0f67-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b0f67-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0f67-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b0f67-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0f67-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b0f67-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


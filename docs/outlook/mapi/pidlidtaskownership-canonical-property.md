---
title: Propriedade canônica PidLidTaskOwnership
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOwnership
api_type:
- COM
ms.assetid: 805dcb6c-f405-4c4d-8bca-af4bd9cd44fa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 45fcba3f18aeb9092b71e28a6b68e42ad1abe77d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332106"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="86b24-103">Propriedade canônica PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="86b24-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="86b24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86b24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86b24-105">Indica a função do usuário atual relativo à tarefa.</span><span class="sxs-lookup"><span data-stu-id="86b24-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86b24-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="86b24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86b24-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="86b24-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="86b24-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="86b24-108">Property set:</span></span>  <br/> |<span data-ttu-id="86b24-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="86b24-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="86b24-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="86b24-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="86b24-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="86b24-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="86b24-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="86b24-112">Data type:</span></span>  <br/> |<span data-ttu-id="86b24-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="86b24-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="86b24-114">Área:</span><span class="sxs-lookup"><span data-stu-id="86b24-114">Area:</span></span>  <br/> |<span data-ttu-id="86b24-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="86b24-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86b24-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="86b24-116">Remarks</span></span>

<span data-ttu-id="86b24-117">Essa propriedade deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="86b24-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="86b24-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="86b24-118">**Value**</span></span>|<span data-ttu-id="86b24-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="86b24-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86b24-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="86b24-120">0x00000000</span></span>  <br/> |<span data-ttu-id="86b24-121">A tarefa não foi atribuída.</span><span class="sxs-lookup"><span data-stu-id="86b24-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="86b24-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="86b24-122">0x00000001</span></span>  <br/> |<span data-ttu-id="86b24-123">A tarefa é a cópia da tarefa do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="86b24-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="86b24-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="86b24-124">0x00000002</span></span>  <br/> |<span data-ttu-id="86b24-125">A tarefa é a cópia da tarefa do destinatário da tarefa.</span><span class="sxs-lookup"><span data-stu-id="86b24-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="86b24-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="86b24-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="86b24-127">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="86b24-127">Protocol specifications</span></span>

<span data-ttu-id="86b24-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86b24-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86b24-129">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="86b24-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="86b24-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="86b24-130">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="86b24-131">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="86b24-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="86b24-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="86b24-132">Header files</span></span>

<span data-ttu-id="86b24-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="86b24-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="86b24-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="86b24-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86b24-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="86b24-135">See also</span></span>



[<span data-ttu-id="86b24-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="86b24-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86b24-137">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="86b24-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86b24-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="86b24-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86b24-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="86b24-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


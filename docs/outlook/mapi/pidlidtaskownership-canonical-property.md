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
ms.openlocfilehash: 17f3ac0c5cd6005329212d0dcb458b37bb75f41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768734"
---
# <a name="pidlidtaskownership-canonical-property"></a><span data-ttu-id="0b7ef-103">Propriedade canônica PidLidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="0b7ef-103">PidLidTaskOwnership Canonical Property</span></span>

  
  
<span data-ttu-id="0b7ef-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b7ef-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0b7ef-105">Indica a função do usuário atual em relação a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-105">Indicates the role of the current user relative to the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b7ef-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0b7ef-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b7ef-107">dispidTaskOwnership</span><span class="sxs-lookup"><span data-stu-id="0b7ef-107">dispidTaskOwnership</span></span>  <br/> |
|<span data-ttu-id="0b7ef-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="0b7ef-108">Property set:</span></span>  <br/> |<span data-ttu-id="0b7ef-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0b7ef-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0b7ef-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="0b7ef-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0b7ef-111">0x00008129</span><span class="sxs-lookup"><span data-stu-id="0b7ef-111">0x00008129</span></span>  <br/> |
|<span data-ttu-id="0b7ef-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0b7ef-112">Data type:</span></span>  <br/> |<span data-ttu-id="0b7ef-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b7ef-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b7ef-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0b7ef-114">Area:</span></span>  <br/> |<span data-ttu-id="0b7ef-115">Task</span><span class="sxs-lookup"><span data-stu-id="0b7ef-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b7ef-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b7ef-116">Remarks</span></span>

<span data-ttu-id="0b7ef-117">Esta propriedade deve ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-117">This property must be one of the following values.</span></span>
  
|<span data-ttu-id="0b7ef-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="0b7ef-118">**Value**</span></span>|<span data-ttu-id="0b7ef-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0b7ef-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b7ef-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b7ef-120">0x00000000</span></span>  <br/> |<span data-ttu-id="0b7ef-121">A tarefa não é atribuída.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-121">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="0b7ef-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0b7ef-122">0x00000001</span></span>  <br/> |<span data-ttu-id="0b7ef-123">A tarefa é uma cópia do cedente a tarefa da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-123">The task is the task assigner's copy of the task.</span></span>  <br/> |
|<span data-ttu-id="0b7ef-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0b7ef-124">0x00000002</span></span>  <br/> |<span data-ttu-id="0b7ef-125">A tarefa é uma cópia do destinatário da tarefa da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-125">The task is the task assignee's copy of the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="0b7ef-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b7ef-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b7ef-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b7ef-127">Protocol specifications</span></span>

<span data-ttu-id="0b7ef-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b7ef-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b7ef-129">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-129">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b7ef-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b7ef-130">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b7ef-131">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-131">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b7ef-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b7ef-132">Header files</span></span>

<span data-ttu-id="0b7ef-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b7ef-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b7ef-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0b7ef-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b7ef-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b7ef-135">See also</span></span>



[<span data-ttu-id="0b7ef-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b7ef-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b7ef-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0b7ef-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b7ef-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0b7ef-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b7ef-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0b7ef-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


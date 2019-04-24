---
title: Propriedade canônica PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360064"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="f8789-103">Propriedade canônica PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="f8789-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="f8789-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8789-105">Fornece dicas de otimização sobre os destinatários de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="f8789-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8789-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f8789-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8789-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="f8789-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="f8789-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="f8789-108">Property set:</span></span>  <br/> |<span data-ttu-id="f8789-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="f8789-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="f8789-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="f8789-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f8789-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="f8789-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="f8789-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f8789-112">Data type:</span></span>  <br/> |<span data-ttu-id="f8789-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f8789-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f8789-114">Área:</span><span class="sxs-lookup"><span data-stu-id="f8789-114">Area:</span></span>  <br/> |<span data-ttu-id="f8789-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="f8789-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8789-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8789-116">Remarks</span></span>

<span data-ttu-id="f8789-117">Se definido, essa propriedade deve ser definida como uma operação bit a bit **ou** como zero ou mais dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="f8789-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="f8789-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f8789-118">**Name**</span></span>|<span data-ttu-id="f8789-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f8789-119">**Value**</span></span>|<span data-ttu-id="f8789-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f8789-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8789-121">Enviado</span><span class="sxs-lookup"><span data-stu-id="f8789-121">Sent</span></span>  <br/> |<span data-ttu-id="f8789-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f8789-122">0x00000001</span></span>  <br/> |<span data-ttu-id="f8789-123">A tarefa tem vários destinatários primários.</span><span class="sxs-lookup"><span data-stu-id="f8789-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="f8789-124">Received</span><span class="sxs-lookup"><span data-stu-id="f8789-124">Received</span></span>  <br/> |<span data-ttu-id="f8789-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f8789-125">0x00000002</span></span>  <br/> |<span data-ttu-id="f8789-126">Embora a dica sent não estivesse presente, o cliente detectou que a tarefa tem vários destinatários primários.</span><span class="sxs-lookup"><span data-stu-id="f8789-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="f8789-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="f8789-127">Reserved</span></span>  <br/> |<span data-ttu-id="f8789-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="f8789-128">0x00000004</span></span>  <br/> |<span data-ttu-id="f8789-129">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="f8789-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f8789-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8789-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8789-131">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="f8789-131">Protocol specifications</span></span>

<span data-ttu-id="f8789-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8789-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8789-133">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="f8789-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8789-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8789-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8789-135">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="f8789-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8789-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8789-136">Header files</span></span>

<span data-ttu-id="f8789-137">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f8789-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8789-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f8789-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8789-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8789-139">See also</span></span>



[<span data-ttu-id="f8789-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f8789-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8789-141">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="f8789-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8789-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f8789-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8789-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f8789-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


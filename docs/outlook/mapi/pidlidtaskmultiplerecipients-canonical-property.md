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
ms.openlocfilehash: f20c3e988c0a0461a966a109a8d345c22e1fccee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585735"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="d3cbb-103">Propriedade canônica PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="d3cbb-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="d3cbb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3cbb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3cbb-105">Fornece dicas de otimização sobre os destinatários de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3cbb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d3cbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d3cbb-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="d3cbb-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="d3cbb-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="d3cbb-108">Property set:</span></span>  <br/> |<span data-ttu-id="d3cbb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="d3cbb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="d3cbb-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="d3cbb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d3cbb-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="d3cbb-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="d3cbb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d3cbb-112">Data type:</span></span>  <br/> |<span data-ttu-id="d3cbb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d3cbb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d3cbb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="d3cbb-114">Area:</span></span>  <br/> |<span data-ttu-id="d3cbb-115">Task</span><span class="sxs-lookup"><span data-stu-id="d3cbb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3cbb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3cbb-116">Remarks</span></span>

<span data-ttu-id="d3cbb-117">Se definido, essa propriedade deverá ser definida como uma operação **OR** bit a bit de zero ou mais dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="d3cbb-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="d3cbb-118">**Name**</span></span>|<span data-ttu-id="d3cbb-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3cbb-119">**Value**</span></span>|<span data-ttu-id="d3cbb-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d3cbb-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d3cbb-121">Enviado</span><span class="sxs-lookup"><span data-stu-id="d3cbb-121">Sent</span></span>  <br/> |<span data-ttu-id="d3cbb-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d3cbb-122">0x00000001</span></span>  <br/> |<span data-ttu-id="d3cbb-123">A tarefa possui vários destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="d3cbb-124">Received</span><span class="sxs-lookup"><span data-stu-id="d3cbb-124">Received</span></span>  <br/> |<span data-ttu-id="d3cbb-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d3cbb-125">0x00000002</span></span>  <br/> |<span data-ttu-id="d3cbb-126">Embora a dica Sent não estava presente, o cliente detectou que a tarefa tem vários destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="d3cbb-127">Reservado</span><span class="sxs-lookup"><span data-stu-id="d3cbb-127">Reserved</span></span>  <br/> |<span data-ttu-id="d3cbb-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d3cbb-128">0x00000004</span></span>  <br/> |<span data-ttu-id="d3cbb-129">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d3cbb-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3cbb-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d3cbb-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d3cbb-131">Protocol specifications</span></span>

<span data-ttu-id="d3cbb-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3cbb-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3cbb-133">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d3cbb-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d3cbb-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d3cbb-135">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d3cbb-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d3cbb-136">Header files</span></span>

<span data-ttu-id="d3cbb-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d3cbb-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="d3cbb-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d3cbb-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d3cbb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3cbb-139">See also</span></span>



[<span data-ttu-id="d3cbb-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d3cbb-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d3cbb-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d3cbb-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d3cbb-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d3cbb-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d3cbb-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d3cbb-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


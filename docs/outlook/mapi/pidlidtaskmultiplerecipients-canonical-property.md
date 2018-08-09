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
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768716"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="5dd62-103">Propriedade canônica PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="5dd62-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="5dd62-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5dd62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5dd62-105">Fornece dicas de otimização sobre os destinatários de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="5dd62-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dd62-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="5dd62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5dd62-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="5dd62-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="5dd62-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="5dd62-108">Property set:</span></span>  <br/> |<span data-ttu-id="5dd62-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5dd62-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5dd62-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="5dd62-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5dd62-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="5dd62-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="5dd62-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="5dd62-112">Data type:</span></span>  <br/> |<span data-ttu-id="5dd62-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5dd62-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5dd62-114">Área:</span><span class="sxs-lookup"><span data-stu-id="5dd62-114">Area:</span></span>  <br/> |<span data-ttu-id="5dd62-115">Task</span><span class="sxs-lookup"><span data-stu-id="5dd62-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dd62-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dd62-116">Remarks</span></span>

<span data-ttu-id="5dd62-117">Se definido, essa propriedade deverá ser definida como uma operação **OR** bit a bit de zero ou mais dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="5dd62-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="5dd62-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="5dd62-118">**Name**</span></span>|<span data-ttu-id="5dd62-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5dd62-119">**Value**</span></span>|<span data-ttu-id="5dd62-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5dd62-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5dd62-121">Enviado</span><span class="sxs-lookup"><span data-stu-id="5dd62-121">Sent</span></span>  <br/> |<span data-ttu-id="5dd62-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5dd62-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5dd62-123">A tarefa possui vários destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="5dd62-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="5dd62-124">Received</span><span class="sxs-lookup"><span data-stu-id="5dd62-124">Received</span></span>  <br/> |<span data-ttu-id="5dd62-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5dd62-125">0x00000002</span></span>  <br/> |<span data-ttu-id="5dd62-126">Embora a dica Sent não estava presente, o cliente detectou que a tarefa tem vários destinatários principais.</span><span class="sxs-lookup"><span data-stu-id="5dd62-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="5dd62-127">Reservado</span><span class="sxs-lookup"><span data-stu-id="5dd62-127">Reserved</span></span>  <br/> |<span data-ttu-id="5dd62-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5dd62-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5dd62-129">Esse valor é reservado.</span><span class="sxs-lookup"><span data-stu-id="5dd62-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5dd62-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dd62-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5dd62-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="5dd62-131">Protocol specifications</span></span>

<span data-ttu-id="5dd62-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dd62-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dd62-133">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5dd62-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5dd62-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5dd62-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5dd62-135">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="5dd62-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5dd62-136">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5dd62-136">Header files</span></span>

<span data-ttu-id="5dd62-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5dd62-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="5dd62-138">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="5dd62-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5dd62-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dd62-139">See also</span></span>



[<span data-ttu-id="5dd62-140">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5dd62-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5dd62-141">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="5dd62-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5dd62-142">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="5dd62-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5dd62-143">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="5dd62-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


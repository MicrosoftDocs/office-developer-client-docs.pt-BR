---
title: Propriedade canônica PidLidPercentComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf4edcc22deafe47fccb4fa44782b33aa18b8cec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587177"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="3b162-103">Propriedade canônica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="3b162-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="3b162-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b162-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b162-105">Indica que o progresso do usuário tornou-se em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="3b162-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b162-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3b162-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b162-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="3b162-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="3b162-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="3b162-108">Property set:</span></span>  <br/> |<span data-ttu-id="3b162-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3b162-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3b162-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="3b162-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3b162-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="3b162-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="3b162-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3b162-112">Data type:</span></span>  <br/> |<span data-ttu-id="3b162-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="3b162-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="3b162-114">Área:</span><span class="sxs-lookup"><span data-stu-id="3b162-114">Area:</span></span>  <br/> |<span data-ttu-id="3b162-115">Task</span><span class="sxs-lookup"><span data-stu-id="3b162-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b162-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b162-116">Remarks</span></span>

<span data-ttu-id="3b162-117">O valor dessa propriedade deve ser um número maior ou igual a 0,0 e menor ou igual a 1.0, onde 1.0 indica que o trabalho está concluído e 0,0 indica que o trabalho não tiver começado.</span><span class="sxs-lookup"><span data-stu-id="3b162-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="3b162-118">Para um objeto de mensagem sinalizados por vez, o valor dessa propriedade deve ser definido a 1,0 se o objeto está sinalizado concluído e deve ser definido como 0,0 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3b162-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3b162-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b162-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b162-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="3b162-120">Protocol specifications</span></span>

<span data-ttu-id="3b162-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b162-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b162-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-123">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-124">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="3b162-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="3b162-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-125">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-126">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="3b162-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="3b162-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-127">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-128">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3b162-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="3b162-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-130">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="3b162-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3b162-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b162-131">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b162-132">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="3b162-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b162-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3b162-133">Header files</span></span>

<span data-ttu-id="3b162-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b162-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b162-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3b162-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b162-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b162-136">See also</span></span>



[<span data-ttu-id="3b162-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3b162-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b162-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3b162-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b162-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3b162-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b162-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3b162-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


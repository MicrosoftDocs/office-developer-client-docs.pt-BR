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
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357971"
---
# <a name="pidlidpercentcomplete-canonical-property"></a><span data-ttu-id="0fafa-103">Propriedade canônica PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="0fafa-103">PidLidPercentComplete Canonical Property</span></span>

  
  
<span data-ttu-id="0fafa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fafa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fafa-105">Indica o progresso que o usuário fez em uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="0fafa-105">Indicates the progress the user has made on a task.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fafa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0fafa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0fafa-107">dispidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="0fafa-107">dispidPercentComplete</span></span>  <br/> |
|<span data-ttu-id="0fafa-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="0fafa-108">Property set:</span></span>  <br/> |<span data-ttu-id="0fafa-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="0fafa-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="0fafa-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="0fafa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0fafa-111">0x00008102</span><span class="sxs-lookup"><span data-stu-id="0fafa-111">0x00008102</span></span>  <br/> |
|<span data-ttu-id="0fafa-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0fafa-112">Data type:</span></span>  <br/> |<span data-ttu-id="0fafa-113">PT_R8</span><span class="sxs-lookup"><span data-stu-id="0fafa-113">PT_R8</span></span>  <br/> |
|<span data-ttu-id="0fafa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="0fafa-114">Area:</span></span>  <br/> |<span data-ttu-id="0fafa-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="0fafa-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fafa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fafa-116">Remarks</span></span>

<span data-ttu-id="0fafa-117">O valor dessa propriedade deve ser um número maior ou igual a 0,0 e menor ou igual a 1,0, onde 1,0 indica que o trabalho foi concluído e 0,0 indica que o trabalho não começou.</span><span class="sxs-lookup"><span data-stu-id="0fafa-117">The value of this property must be a number greater than or equal to 0.0 and less than or equal to 1.0, where 1.0 indicates that work is completed and 0.0 indicates that work has not begun.</span></span>
  
<span data-ttu-id="0fafa-118">Para um objeto de mensagem sinalizado com tempo, o valor dessa propriedade deverá ser definido como 1,0 se o objeto estiver sinalizado como concluído e, caso contrário, deverá ser definido como 0,0.</span><span class="sxs-lookup"><span data-stu-id="0fafa-118">For a time-flagged message object, the value of this property must be set to 1.0 if the object is flagged completed, and should be set to 0.0 otherwise.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0fafa-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fafa-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0fafa-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0fafa-120">Protocol specifications</span></span>

<span data-ttu-id="0fafa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0fafa-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0fafa-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-124">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="0fafa-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="0fafa-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-125">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-126">Especifica as propriedades e operações relacionadas à sinalização.</span><span class="sxs-lookup"><span data-stu-id="0fafa-126">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="0fafa-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-127">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-128">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0fafa-128">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="0fafa-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-130">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="0fafa-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="0fafa-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0fafa-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0fafa-132">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="0fafa-132">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0fafa-133">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="0fafa-133">Header files</span></span>

<span data-ttu-id="0fafa-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0fafa-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="0fafa-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0fafa-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fafa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fafa-136">See also</span></span>



[<span data-ttu-id="0fafa-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0fafa-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0fafa-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0fafa-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0fafa-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0fafa-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0fafa-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0fafa-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


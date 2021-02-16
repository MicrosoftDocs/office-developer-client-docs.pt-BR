---
title: Propriedade canônica PidLidTaskFCreator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFCreator
api_type:
- COM
ms.assetid: bb88750b-4773-4241-aa38-462a2634dbcb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dfb49fafcc2dc368e84786b526869e0447ccaf8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303077"
---
# <a name="pidlidtaskfcreator-canonical-property"></a><span data-ttu-id="bd6d6-103">Propriedade canônica PidLidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="bd6d6-103">PidLidTaskFCreator Canonical Property</span></span>

  
  
<span data-ttu-id="bd6d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd6d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd6d6-105">Indica que a tarefa foi originalmente criada pelo usuário ou agente do usuário atual, em vez de processar uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-105">Indicates the task was originally created by the current user or user agent instead of by processing a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bd6d6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="bd6d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bd6d6-107">dispidTaskFCreator</span><span class="sxs-lookup"><span data-stu-id="bd6d6-107">dispidTaskFCreator</span></span>  <br/> |
|<span data-ttu-id="bd6d6-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="bd6d6-108">Property set:</span></span>  <br/> |<span data-ttu-id="bd6d6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="bd6d6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="bd6d6-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="bd6d6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="bd6d6-111">0x0000811E</span><span class="sxs-lookup"><span data-stu-id="bd6d6-111">0x0000811E</span></span>  <br/> |
|<span data-ttu-id="bd6d6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="bd6d6-112">Data type:</span></span>  <br/> |<span data-ttu-id="bd6d6-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bd6d6-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bd6d6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="bd6d6-114">Area:</span></span>  <br/> |<span data-ttu-id="bd6d6-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="bd6d6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd6d6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd6d6-116">Remarks</span></span>

<span data-ttu-id="bd6d6-117">O cliente define essa propriedade como TRUE quando o usuário cria a tarefa e como FALSE quando a tarefa é atribuída por outro usuário.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-117">The client sets this property to TRUE when the user creates the task and to FALSE when the task is assigned by another user.</span></span> <span data-ttu-id="bd6d6-118">Se essa propriedade for deixada desalinhada, será assumido um valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-118">If this property is left unset, a value of TRUE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bd6d6-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd6d6-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bd6d6-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="bd6d6-120">Protocol specifications</span></span>

<span data-ttu-id="bd6d6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd6d6-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd6d6-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bd6d6-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bd6d6-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bd6d6-124">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-124">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bd6d6-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="bd6d6-125">Header files</span></span>

<span data-ttu-id="bd6d6-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd6d6-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="bd6d6-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd6d6-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bd6d6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd6d6-128">See also</span></span>



[<span data-ttu-id="bd6d6-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="bd6d6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bd6d6-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="bd6d6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bd6d6-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="bd6d6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bd6d6-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="bd6d6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


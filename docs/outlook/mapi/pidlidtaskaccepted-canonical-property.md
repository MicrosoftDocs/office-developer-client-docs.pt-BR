---
title: Propriedade canônica PidLidTaskAccepted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskAccepted
api_type:
- COM
ms.assetid: 8e31f893-b639-43da-a535-662153c82d82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0172bf0d69c3f345b592364be754f58c9e7a4420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331280"
---
# <a name="pidlidtaskaccepted-canonical-property"></a><span data-ttu-id="32ebb-103">Propriedade canônica PidLidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="32ebb-103">PidLidTaskAccepted Canonical Property</span></span>

  
  
<span data-ttu-id="32ebb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32ebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32ebb-105">Indica se um destinatário da tarefa respondeu a uma solicitação de tarefa.</span><span class="sxs-lookup"><span data-stu-id="32ebb-105">Indicates whether a task assignee has replied to a task request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="32ebb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="32ebb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="32ebb-107">dispidTaskAccepted</span><span class="sxs-lookup"><span data-stu-id="32ebb-107">dispidTaskAccepted</span></span>  <br/> |
|<span data-ttu-id="32ebb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="32ebb-108">Property set:</span></span>  <br/> |<span data-ttu-id="32ebb-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="32ebb-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="32ebb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="32ebb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="32ebb-111">0x00008108</span><span class="sxs-lookup"><span data-stu-id="32ebb-111">0x00008108</span></span>  <br/> |
|<span data-ttu-id="32ebb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="32ebb-112">Data type:</span></span>  <br/> |<span data-ttu-id="32ebb-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="32ebb-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="32ebb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="32ebb-114">Area:</span></span>  <br/> |<span data-ttu-id="32ebb-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="32ebb-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32ebb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ebb-116">Remarks</span></span>

<span data-ttu-id="32ebb-117">O cliente define essa propriedade como FALSE para uma nova tarefa ou define essa propriedade como TRUE quando uma tarefa é aceita ou rejeitada.</span><span class="sxs-lookup"><span data-stu-id="32ebb-117">The client sets this property to FALSE for a new task, or the client sets this property to TRUE when a task is either accepted or rejected.</span></span> <span data-ttu-id="32ebb-118">Se a propriedade for deixada desalinhada, será assumido um valor FALSO.</span><span class="sxs-lookup"><span data-stu-id="32ebb-118">If the property is left unset, a value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="32ebb-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="32ebb-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="32ebb-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="32ebb-120">Protocol specifications</span></span>

<span data-ttu-id="32ebb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ebb-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ebb-122">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="32ebb-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="32ebb-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="32ebb-123">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="32ebb-124">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="32ebb-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="32ebb-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="32ebb-125">Header files</span></span>

<span data-ttu-id="32ebb-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="32ebb-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="32ebb-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="32ebb-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="32ebb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="32ebb-128">See also</span></span>



[<span data-ttu-id="32ebb-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="32ebb-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="32ebb-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="32ebb-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="32ebb-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="32ebb-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="32ebb-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="32ebb-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidLidTaskGlobalId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskGlobalId
api_type:
- COM
ms.assetid: 369d8c78-3cf6-4a55-ba14-9da0377d6ccf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 295eb9dcc6da7b0fb6c6fd7ea0b73134ffaadb3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303014"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="906fd-103">Propriedade canônica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="906fd-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="906fd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="906fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="906fd-105">Localiza uma tarefa existente, usando um GUID, mediante o recebimento de uma resposta de tarefa ou atualização de tarefa.</span><span class="sxs-lookup"><span data-stu-id="906fd-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="906fd-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="906fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="906fd-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="906fd-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="906fd-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="906fd-108">Property set:</span></span>  <br/> |<span data-ttu-id="906fd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="906fd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="906fd-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="906fd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="906fd-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="906fd-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="906fd-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="906fd-112">Data type:</span></span>  <br/> |<span data-ttu-id="906fd-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="906fd-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="906fd-114">Área:</span><span class="sxs-lookup"><span data-stu-id="906fd-114">Area:</span></span>  <br/> |<span data-ttu-id="906fd-115">Tarefas</span><span class="sxs-lookup"><span data-stu-id="906fd-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="906fd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="906fd-116">Remarks</span></span>

<span data-ttu-id="906fd-117">Essa propriedade é deixada sem atribuições para tarefas não atribuídas.</span><span class="sxs-lookup"><span data-stu-id="906fd-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="906fd-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="906fd-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="906fd-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="906fd-119">Protocol specifications</span></span>

<span data-ttu-id="906fd-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="906fd-120">[[MS-OXPROPS] ](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="906fd-121">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="906fd-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="906fd-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="906fd-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="906fd-123">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="906fd-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="906fd-124">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="906fd-124">Header files</span></span>

<span data-ttu-id="906fd-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="906fd-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="906fd-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="906fd-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="906fd-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="906fd-127">See also</span></span>



[<span data-ttu-id="906fd-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="906fd-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="906fd-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="906fd-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="906fd-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="906fd-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="906fd-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="906fd-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


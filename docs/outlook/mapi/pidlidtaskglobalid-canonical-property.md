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
ms.openlocfilehash: 33f3b8e7d3d0e0d4461c947aa8e9b3ee66373d2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768695"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="a1448-103">Propriedade canônica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="a1448-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="a1448-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1448-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1448-105">Localiza uma tarefa existente, usando um GUID, no recebimento de uma atualização de tarefa ou uma resposta de tarefa.</span><span class="sxs-lookup"><span data-stu-id="a1448-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a1448-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a1448-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a1448-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="a1448-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="a1448-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="a1448-108">Property set:</span></span>  <br/> |<span data-ttu-id="a1448-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a1448-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a1448-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="a1448-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a1448-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="a1448-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="a1448-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a1448-112">Data type:</span></span>  <br/> |<span data-ttu-id="a1448-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a1448-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a1448-114">Área:</span><span class="sxs-lookup"><span data-stu-id="a1448-114">Area:</span></span>  <br/> |<span data-ttu-id="a1448-115">Task</span><span class="sxs-lookup"><span data-stu-id="a1448-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1448-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1448-116">Remarks</span></span>

<span data-ttu-id="a1448-117">Essa propriedade é da esquerda não definida para tarefas não atribuídas.</span><span class="sxs-lookup"><span data-stu-id="a1448-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a1448-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1448-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a1448-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a1448-119">Protocol specifications</span></span>

<span data-ttu-id="a1448-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1448-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1448-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a1448-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a1448-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a1448-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a1448-123">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="a1448-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a1448-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a1448-124">Header files</span></span>

<span data-ttu-id="a1448-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1448-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a1448-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a1448-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a1448-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1448-127">See also</span></span>



[<span data-ttu-id="a1448-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a1448-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a1448-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a1448-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a1448-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a1448-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a1448-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a1448-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


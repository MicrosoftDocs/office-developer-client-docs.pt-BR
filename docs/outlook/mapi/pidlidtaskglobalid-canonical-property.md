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
ms.openlocfilehash: 4f91b4cdeb301eba6eb9753fc5e7dc3e3d5d892c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592616"
---
# <a name="pidlidtaskglobalid-canonical-property"></a><span data-ttu-id="17a83-103">Propriedade canônica PidLidTaskGlobalId</span><span class="sxs-lookup"><span data-stu-id="17a83-103">PidLidTaskGlobalId Canonical Property</span></span>

  
  
<span data-ttu-id="17a83-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17a83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17a83-105">Localiza uma tarefa existente, usando um GUID, no recebimento de uma atualização de tarefa ou uma resposta de tarefa.</span><span class="sxs-lookup"><span data-stu-id="17a83-105">Locates an existing task, by using a GUID, upon receipt of a task response or task update.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17a83-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="17a83-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17a83-107">dispidTaskGlobalObjId</span><span class="sxs-lookup"><span data-stu-id="17a83-107">dispidTaskGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="17a83-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="17a83-108">Property set:</span></span>  <br/> |<span data-ttu-id="17a83-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="17a83-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="17a83-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="17a83-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="17a83-111">0x00008519</span><span class="sxs-lookup"><span data-stu-id="17a83-111">0x00008519</span></span>  <br/> |
|<span data-ttu-id="17a83-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="17a83-112">Data type:</span></span>  <br/> |<span data-ttu-id="17a83-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="17a83-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="17a83-114">Área:</span><span class="sxs-lookup"><span data-stu-id="17a83-114">Area:</span></span>  <br/> |<span data-ttu-id="17a83-115">Task</span><span class="sxs-lookup"><span data-stu-id="17a83-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17a83-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="17a83-116">Remarks</span></span>

<span data-ttu-id="17a83-117">Essa propriedade é da esquerda não definida para tarefas não atribuídas.</span><span class="sxs-lookup"><span data-stu-id="17a83-117">This property is left unset for unassigned tasks.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="17a83-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="17a83-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17a83-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="17a83-119">Protocol specifications</span></span>

<span data-ttu-id="17a83-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17a83-120">[[MS-OXPROPS] ](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17a83-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="17a83-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17a83-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17a83-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17a83-123">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="17a83-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17a83-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="17a83-124">Header files</span></span>

<span data-ttu-id="17a83-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17a83-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="17a83-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="17a83-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17a83-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="17a83-127">See also</span></span>



[<span data-ttu-id="17a83-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="17a83-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17a83-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="17a83-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17a83-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="17a83-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17a83-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="17a83-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


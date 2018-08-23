---
title: Propriedade canônica PidLidTaskDateCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskDateCompleted
api_type:
- COM
ms.assetid: ae384529-55e2-4da1-9a41-acc292591a7c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 97d541279f052099498cdf7bfd374a95238a376d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584216"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="de439-103">Propriedade canônica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="de439-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="de439-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de439-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de439-105">Especifica a data quando o usuário conclui a tarefa.</span><span class="sxs-lookup"><span data-stu-id="de439-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de439-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="de439-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de439-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="de439-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="de439-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="de439-108">Property set:</span></span>  <br/> |<span data-ttu-id="de439-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="de439-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="de439-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="de439-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="de439-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="de439-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="de439-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="de439-112">Data type:</span></span>  <br/> |<span data-ttu-id="de439-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="de439-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="de439-114">Área:</span><span class="sxs-lookup"><span data-stu-id="de439-114">Area:</span></span>  <br/> |<span data-ttu-id="de439-115">Task</span><span class="sxs-lookup"><span data-stu-id="de439-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de439-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="de439-116">Remarks</span></span>

<span data-ttu-id="de439-117">Se definido, esta propriedade deve ter um componente de hora de meia-noite no fuso horário local, convertido para o tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="de439-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="de439-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="de439-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="de439-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="de439-119">Protocol specifications</span></span>

<span data-ttu-id="de439-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de439-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de439-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="de439-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="de439-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="de439-122">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="de439-123">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="de439-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="de439-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de439-124">Header files</span></span>

<span data-ttu-id="de439-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="de439-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="de439-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="de439-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de439-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="de439-127">See also</span></span>



[<span data-ttu-id="de439-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="de439-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de439-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="de439-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de439-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="de439-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de439-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="de439-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


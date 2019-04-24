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
ms.openlocfilehash: 3096e7ab2133d2984be0534cb091d61d2c7157bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303210"
---
# <a name="pidlidtaskdatecompleted-canonical-property"></a><span data-ttu-id="af10e-103">Propriedade canônica PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="af10e-103">PidLidTaskDateCompleted Canonical Property</span></span>

  
  
<span data-ttu-id="af10e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af10e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af10e-105">Especifica a data em que o usuário conclui a tarefa.</span><span class="sxs-lookup"><span data-stu-id="af10e-105">Specifies the date when the user completes the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="af10e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="af10e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af10e-107">dispidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="af10e-107">dispidTaskDateCompleted</span></span>  <br/> |
|<span data-ttu-id="af10e-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="af10e-108">Property set:</span></span>  <br/> |<span data-ttu-id="af10e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="af10e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="af10e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="af10e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="af10e-111">0x0000810F</span><span class="sxs-lookup"><span data-stu-id="af10e-111">0x0000810F</span></span>  <br/> |
|<span data-ttu-id="af10e-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="af10e-112">Data type:</span></span>  <br/> |<span data-ttu-id="af10e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="af10e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="af10e-114">Área:</span><span class="sxs-lookup"><span data-stu-id="af10e-114">Area:</span></span>  <br/> |<span data-ttu-id="af10e-115">Tarefa</span><span class="sxs-lookup"><span data-stu-id="af10e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af10e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="af10e-116">Remarks</span></span>

<span data-ttu-id="af10e-117">Se definido, essa propriedade deve ter um componente de tempo da meia-noite no fuso horário local, convertido no tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="af10e-117">If set, this property must have a time component of midnight in the local time zone, converted to Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="af10e-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="af10e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af10e-119">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="af10e-119">Protocol specifications</span></span>

<span data-ttu-id="af10e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af10e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af10e-121">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="af10e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af10e-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af10e-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af10e-123">Define vários objetos que modelam o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="af10e-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="af10e-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af10e-124">Header files</span></span>

<span data-ttu-id="af10e-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="af10e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="af10e-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="af10e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af10e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="af10e-127">See also</span></span>



[<span data-ttu-id="af10e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="af10e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af10e-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="af10e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af10e-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="af10e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af10e-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="af10e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


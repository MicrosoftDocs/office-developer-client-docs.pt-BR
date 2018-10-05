---
title: Propriedade canônica PidLidTaskEstimatedEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskEstimatedEffort
api_type:
- COM
ms.assetid: c84167d8-f726-45c6-9b21-bcde64473148
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5700ab6baaab2a5e73448582a855e6f243d5361d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382796"
---
# <a name="pidlidtaskestimatedeffort-canonical-property"></a><span data-ttu-id="648c6-103">Propriedade canônica PidLidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="648c6-103">PidLidTaskEstimatedEffort Canonical Property</span></span>

  
  
<span data-ttu-id="648c6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="648c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="648c6-105">Indica a quantidade de tempo, em minutos, que o usuário espera para executar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="648c6-105">Indicates the amount of time, in minutes, that the user expects to perform a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="648c6-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="648c6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="648c6-107">dispidTaskEstimatedEffort</span><span class="sxs-lookup"><span data-stu-id="648c6-107">dispidTaskEstimatedEffort</span></span>  <br/> |
|<span data-ttu-id="648c6-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="648c6-108">Property set:</span></span>  <br/> |<span data-ttu-id="648c6-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="648c6-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="648c6-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="648c6-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="648c6-111">0x00008111</span><span class="sxs-lookup"><span data-stu-id="648c6-111">0x00008111</span></span>  <br/> |
|<span data-ttu-id="648c6-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="648c6-112">Data type:</span></span>  <br/> |<span data-ttu-id="648c6-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="648c6-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="648c6-114">Área:</span><span class="sxs-lookup"><span data-stu-id="648c6-114">Area:</span></span>  <br/> |<span data-ttu-id="648c6-115">Task</span><span class="sxs-lookup"><span data-stu-id="648c6-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="648c6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="648c6-116">Remarks</span></span>

<span data-ttu-id="648c6-117">O valor deve ser maior ou igual a 0 e menor que 0x5AE980DF (1,525,252,319), onde o 480 minutos igual a um dia e 2400 minutos igual uma semana (oito horas em um dia de trabalho e cinco dias em uma semana de trabalho).</span><span class="sxs-lookup"><span data-stu-id="648c6-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="648c6-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="648c6-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="648c6-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="648c6-119">Protocol specifications</span></span>

<span data-ttu-id="648c6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="648c6-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="648c6-121">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="648c6-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="648c6-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="648c6-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="648c6-123">Define a vários objetos que modelar o equivalente eletrônico de tarefas, atribuições de tarefas e atualizações de tarefas.</span><span class="sxs-lookup"><span data-stu-id="648c6-123">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="648c6-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="648c6-124">Header files</span></span>

<span data-ttu-id="648c6-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="648c6-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="648c6-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="648c6-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="648c6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="648c6-127">See also</span></span>



[<span data-ttu-id="648c6-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="648c6-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="648c6-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="648c6-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="648c6-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="648c6-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="648c6-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="648c6-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


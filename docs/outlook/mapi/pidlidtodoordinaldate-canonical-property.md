---
title: Propriedade canônica PidLidToDoOrdinalDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoOrdinalDate
api_type:
- COM
ms.assetid: b6a500fc-07f4-4788-ae46-d179a96a48e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b19f36337459753e153a96021b1d70308b374bed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577755"
---
# <a name="pidlidtodoordinaldate-canonical-property"></a><span data-ttu-id="10ab2-103">Propriedade canônica PidLidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="10ab2-103">PidLidToDoOrdinalDate Canonical Property</span></span>

  
  
<span data-ttu-id="10ab2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10ab2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10ab2-105">Determina a ordem de classificação dos objetos em uma lista de tarefas pendentes consolidada.</span><span class="sxs-lookup"><span data-stu-id="10ab2-105">Determines the sort order of objects in a consolidated to-do list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10ab2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="10ab2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10ab2-107">dispidToDoOrdinalDate</span><span class="sxs-lookup"><span data-stu-id="10ab2-107">dispidToDoOrdinalDate</span></span>  <br/> |
|<span data-ttu-id="10ab2-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="10ab2-108">Property set:</span></span>  <br/> |<span data-ttu-id="10ab2-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="10ab2-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="10ab2-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="10ab2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10ab2-111">0x000085A0</span><span class="sxs-lookup"><span data-stu-id="10ab2-111">0x000085A0</span></span>  <br/> |
|<span data-ttu-id="10ab2-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="10ab2-112">Data type:</span></span>  <br/> |<span data-ttu-id="10ab2-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="10ab2-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="10ab2-114">Área:</span><span class="sxs-lookup"><span data-stu-id="10ab2-114">Area:</span></span>  <br/> |<span data-ttu-id="10ab2-115">Task</span><span class="sxs-lookup"><span data-stu-id="10ab2-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10ab2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="10ab2-116">Remarks</span></span>

<span data-ttu-id="10ab2-117">Quando um objeto está sinalizado, essa propriedade deverá ser definida para a hora atual no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="10ab2-117">When an object is flagged, this property should be set to the current time in Coordinated Universal Time (UTC).</span></span> 
  
<span data-ttu-id="10ab2-118">Se o cliente permite que o usuário reordenar tarefas dentro da lista de tarefas consolidada via arrastando ou outros mecanismos, eles podem usar qualquer algoritmo adequado para determinar o novo valor dessa propriedade para que a tarefa seja exibido no lugar correto quando essa propriedade é usada como um CL campo Ting.</span><span class="sxs-lookup"><span data-stu-id="10ab2-118">If the client allows a user to reorder tasks within the consolidated task list via dragging or other mechanisms, they can use any suitable algorithm to determine the new value of this property so that the task appears in the correct place when this property is used as a sorting field.</span></span>
  
<span data-ttu-id="10ab2-119">Quando essa propriedade é usada para classificar os objetos e a classificação dos resultados em uma ligação, a propriedade **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) é usada como um separador de tie.</span><span class="sxs-lookup"><span data-stu-id="10ab2-119">When this property is used to sort objects and the sort results in a tie, the **dispidToDoSubOrdinal** ([PidLidToDoSubOrdinal](pidlidtodosubordinal-canonical-property.md)) property is used as a tie breaker.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10ab2-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="10ab2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10ab2-121">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="10ab2-121">Protocol specifications</span></span>

<span data-ttu-id="10ab2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10ab2-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10ab2-123">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="10ab2-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10ab2-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10ab2-124">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10ab2-125">Especifica as propriedades e operações relacionadas a sinalização.</span><span class="sxs-lookup"><span data-stu-id="10ab2-125">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10ab2-126">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10ab2-126">Header files</span></span>

<span data-ttu-id="10ab2-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10ab2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="10ab2-128">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="10ab2-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10ab2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="10ab2-129">See also</span></span>



[<span data-ttu-id="10ab2-130">Propriedade canônica PidLidToDoSubOrdinal</span><span class="sxs-lookup"><span data-stu-id="10ab2-130">PidLidToDoSubOrdinal Canonical Property</span></span>](pidlidtodosubordinal-canonical-property.md)


[<span data-ttu-id="10ab2-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="10ab2-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10ab2-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="10ab2-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10ab2-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="10ab2-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10ab2-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="10ab2-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


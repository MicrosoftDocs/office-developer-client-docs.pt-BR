---
title: Propriedade canônica PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391175"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="7d00f-103">Propriedade canônica PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="7d00f-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="7d00f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d00f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d00f-105">Representa o número de unidades de tempo que são usados para determinar a quantidade de tempo que um item permanece em uma pasta antes do item será arquivado.</span><span class="sxs-lookup"><span data-stu-id="7d00f-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7d00f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7d00f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d00f-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="7d00f-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="7d00f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7d00f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d00f-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="7d00f-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="7d00f-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="7d00f-110">Property type:</span></span>  <br/> |<span data-ttu-id="7d00f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7d00f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7d00f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7d00f-112">Area:</span></span>  <br/> |<span data-ttu-id="7d00f-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="7d00f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d00f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d00f-114">Remarks</span></span>

<span data-ttu-id="7d00f-115">O período de tempo que um item permanece em uma pasta antes do item será arquivado é determinado pelo duas propriedades, **PR_AGING_PERIOD** e **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="7d00f-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="7d00f-116">**PR_AGING_GRANULARITY** representa a unidade de tempo em que **PR_AGING_PERIOD** é expresso, ao determinar esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="7d00f-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="7d00f-117">Os valores possíveis para **PR_AGING_GRANULARITY** podem ser uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d00f-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="7d00f-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7d00f-118">**Name**</span></span>|<span data-ttu-id="7d00f-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d00f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d00f-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="7d00f-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="7d00f-121">**PR_AGING_PERIOD** é definido no número de meses.</span><span class="sxs-lookup"><span data-stu-id="7d00f-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="7d00f-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="7d00f-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="7d00f-123">**PR_AGING_PERIOD** é definida em número de semanas.</span><span class="sxs-lookup"><span data-stu-id="7d00f-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="7d00f-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="7d00f-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="7d00f-125">**PR_AGING_PERIOD** é definido no número de dias.</span><span class="sxs-lookup"><span data-stu-id="7d00f-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="7d00f-126">Por exemplo, se um arquivos de pasta é um item somente depois que o item tiver sido na pasta para duas semanas e, em seguida, **PR_AGING_GRANULARITY** **AG_WEEKS** e **PR_AGING_PERIOD** é 2.</span><span class="sxs-lookup"><span data-stu-id="7d00f-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d00f-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d00f-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d00f-128">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7d00f-128">Protocol specifications</span></span>

<span data-ttu-id="7d00f-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d00f-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d00f-130">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7d00f-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="7d00f-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d00f-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d00f-132">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="7d00f-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="7d00f-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d00f-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d00f-134">Especifica as propriedades e operações que são permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="7d00f-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d00f-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7d00f-135">Header files</span></span>

<span data-ttu-id="7d00f-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d00f-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d00f-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7d00f-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d00f-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d00f-138">Mapitags.h</span></span>
  
> <span data-ttu-id="7d00f-139">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7d00f-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d00f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d00f-140">See also</span></span>



[<span data-ttu-id="7d00f-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7d00f-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d00f-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="7d00f-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d00f-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d00f-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d00f-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7d00f-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


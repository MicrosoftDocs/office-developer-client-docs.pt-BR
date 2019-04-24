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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360113"
---
# <a name="pidtagagingperiod-canonical-property"></a><span data-ttu-id="75bab-103">Propriedade canônica PidTagAgingPeriod</span><span class="sxs-lookup"><span data-stu-id="75bab-103">PidTagAgingPeriod Canonical Property</span></span>

  
  
<span data-ttu-id="75bab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75bab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75bab-105">Representa o número de unidades de tempo usadas para determinar o período de tempo durante o qual um item permanecerá em uma pasta antes de o item ser arquivado.</span><span class="sxs-lookup"><span data-stu-id="75bab-105">Represents the number of time units that are used to determine the length of time that an item remains in a folder before the item is archived.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="75bab-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="75bab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75bab-107">PR_AGING_PERIOD</span><span class="sxs-lookup"><span data-stu-id="75bab-107">PR_AGING_PERIOD</span></span>  <br/> |
|<span data-ttu-id="75bab-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="75bab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75bab-109">0x36EC</span><span class="sxs-lookup"><span data-stu-id="75bab-109">0x36EC</span></span>  <br/> |
|<span data-ttu-id="75bab-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="75bab-110">Property type:</span></span>  <br/> |<span data-ttu-id="75bab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="75bab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="75bab-112">Área:</span><span class="sxs-lookup"><span data-stu-id="75bab-112">Area:</span></span>  <br/> |<span data-ttu-id="75bab-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="75bab-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75bab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="75bab-114">Remarks</span></span>

<span data-ttu-id="75bab-115">O período de tempo em que um item permanece em uma pasta antes de o item ser arquivado é determinado por duas propriedades, **PR_AGING_PERIOD** e **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="75bab-115">The length of time that an item remains in a folder before the item is archived is determined by two properties, **PR_AGING_PERIOD** and **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**.</span></span> <span data-ttu-id="75bab-116">**PR_AGING_GRANULARITY** representa a unidade de tempo na qual o **PR_AGING_PERIOD** é expresso, ao determinar esse período de tempo.</span><span class="sxs-lookup"><span data-stu-id="75bab-116">**PR_AGING_GRANULARITY** represents the time unit in which **PR_AGING_PERIOD** is expressed, when determining this length of time.</span></span> 
  
<span data-ttu-id="75bab-117">Os valores possíveis para **PR_AGING_GRANULARITY** podem ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="75bab-117">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
****

|<span data-ttu-id="75bab-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="75bab-118">**Name**</span></span>|<span data-ttu-id="75bab-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75bab-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75bab-120">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="75bab-120">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="75bab-121">**PR_AGING_PERIOD** é definido em número de meses.</span><span class="sxs-lookup"><span data-stu-id="75bab-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="75bab-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="75bab-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="75bab-123">**PR_AGING_PERIOD** é definido em número de semanas.</span><span class="sxs-lookup"><span data-stu-id="75bab-123">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="75bab-124">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="75bab-124">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="75bab-125">**PR_AGING_PERIOD** é definido em número de dias.</span><span class="sxs-lookup"><span data-stu-id="75bab-125">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="75bab-126">Por exemplo, se uma pasta arquivar um item somente depois que o item estiver na pasta por duas semanas, **PR_AGING_GRANULARITY** será **AG_WEEKS** e **PR_AGING_PERIOD** será 2.</span><span class="sxs-lookup"><span data-stu-id="75bab-126">For example, if a folder archives an item only after the item has been in the folder for two weeks, then **PR_AGING_GRANULARITY** is **AG_WEEKS** and **PR_AGING_PERIOD** is 2.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75bab-127">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="75bab-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75bab-128">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="75bab-128">Protocol specifications</span></span>

<span data-ttu-id="75bab-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bab-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bab-130">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="75bab-130">Provides property set definitions.</span></span>
    
<span data-ttu-id="75bab-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bab-131">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bab-132">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="75bab-132">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="75bab-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75bab-133">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75bab-134">Especifica as propriedades e as operações permitidas para os objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="75bab-134">Specifies the properties and operations that are permitted for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75bab-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="75bab-135">Header files</span></span>

<span data-ttu-id="75bab-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="75bab-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="75bab-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="75bab-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="75bab-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="75bab-138">Mapitags.h</span></span>
  
> <span data-ttu-id="75bab-139">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="75bab-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75bab-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="75bab-140">See also</span></span>



[<span data-ttu-id="75bab-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="75bab-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75bab-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="75bab-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75bab-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="75bab-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75bab-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="75bab-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


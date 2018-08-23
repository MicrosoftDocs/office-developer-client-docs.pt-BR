---
title: Propriedade canônica PidTagAgingGranularity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingGranularity
api_type:
- HeaderDef
ms.assetid: b79ec87d-d97c-4e6c-899b-78ebf1b485a7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c1b5b36c3a05ef17e319ef236b032b7d07ce8fa8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589417"
---
# <a name="pidtagaginggranularity-canonical-property"></a><span data-ttu-id="6d7e0-103">Propriedade canônica PidTagAgingGranularity</span><span class="sxs-lookup"><span data-stu-id="6d7e0-103">PidTagAgingGranularity Canonical Property</span></span>

  
  
<span data-ttu-id="6d7e0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d7e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d7e0-105">Representa a unidade de tempo que é usado para determinar a quantidade de tempo que um item permanece em uma pasta antes do item será arquivado.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-105">Represents the unit of time that is used in determining the length of time an item remains in a folder before the item is archived.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d7e0-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6d7e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d7e0-107">PR_AGING_GRANULARITY</span><span class="sxs-lookup"><span data-stu-id="6d7e0-107">PR_AGING_GRANULARITY</span></span>  <br/> |
|<span data-ttu-id="6d7e0-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6d7e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d7e0-109">0x36EE</span><span class="sxs-lookup"><span data-stu-id="6d7e0-109">0x36EE</span></span>  <br/> |
|<span data-ttu-id="6d7e0-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="6d7e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d7e0-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d7e0-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d7e0-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6d7e0-112">Area:</span></span>  <br/> |<span data-ttu-id="6d7e0-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="6d7e0-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d7e0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d7e0-114">Remarks</span></span>

<span data-ttu-id="6d7e0-115">Os valores possíveis para **PR_AGING_GRANULARITY** podem ser uma das opções a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-115">The possible values for **PR_AGING_GRANULARITY** can be one of the following.</span></span> 
  
|<span data-ttu-id="6d7e0-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-116">**Name**</span></span>|<span data-ttu-id="6d7e0-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-117">**Value**</span></span>|<span data-ttu-id="6d7e0-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d7e0-119">**AG_MONTHS**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-119">**AG_MONTHS**</span></span> <br/> |<span data-ttu-id="6d7e0-120">0</span><span class="sxs-lookup"><span data-stu-id="6d7e0-120">0</span></span>  <br/> |<span data-ttu-id="6d7e0-121">**PR_AGING_PERIOD** é definido no número de meses.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-121">**PR_AGING_PERIOD** is defined in number of months.</span></span>  <br/> |
|<span data-ttu-id="6d7e0-122">**AG_WEEKS**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-122">**AG_WEEKS**</span></span> <br/> |<span data-ttu-id="6d7e0-123">1</span><span class="sxs-lookup"><span data-stu-id="6d7e0-123">1</span></span>  <br/> |<span data-ttu-id="6d7e0-124">**PR_AGING_PERIOD** é definida em número de semanas.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-124">**PR_AGING_PERIOD** is defined in number of weeks.</span></span>  <br/> |
|<span data-ttu-id="6d7e0-125">**AG_DAYS**</span><span class="sxs-lookup"><span data-stu-id="6d7e0-125">**AG_DAYS**</span></span> <br/> |<span data-ttu-id="6d7e0-126">2</span><span class="sxs-lookup"><span data-stu-id="6d7e0-126">2</span></span>  <br/> |<span data-ttu-id="6d7e0-127">**PR_AGING_PERIOD** é definido no número de dias.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-127">**PR_AGING_PERIOD** is defined in number of days.</span></span>  <br/> |
   
<span data-ttu-id="6d7e0-128">O período de tempo que um item permanece em uma pasta antes do item será arquivado é determinado pelo duas propriedades, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) e **PR_AGING_GRANULARITY**.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-128">The length of time that an item remains in a folder before the item is archived is determined by two properties, [PR_AGING_PERIOD](pidtagagingperiod-canonical-property.md) and **PR_AGING_GRANULARITY**.</span></span> <span data-ttu-id="6d7e0-129">**PR_AGING_PERIOD** representa o número de unidades de tempo que o item permanecerá na pasta antes que ele é arquivado.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-129">**PR_AGING_PERIOD** represents the number of time units that the item remains in the folder before it is archived.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d7e0-130">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6d7e0-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d7e0-131">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6d7e0-131">Protocol specifications</span></span>

<span data-ttu-id="6d7e0-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d7e0-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d7e0-133">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-133">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d7e0-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d7e0-134">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d7e0-135">Define as estruturas de dados básicos que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-135">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="6d7e0-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d7e0-136">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d7e0-137">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-137">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d7e0-138">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d7e0-138">Header files</span></span>

<span data-ttu-id="6d7e0-139">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d7e0-139">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d7e0-140">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-140">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d7e0-141">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d7e0-141">Mapitags.h</span></span>
  
> <span data-ttu-id="6d7e0-142">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6d7e0-142">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d7e0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d7e0-143">See also</span></span>



[<span data-ttu-id="6d7e0-144">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6d7e0-144">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d7e0-145">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6d7e0-145">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d7e0-146">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6d7e0-146">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d7e0-147">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6d7e0-147">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


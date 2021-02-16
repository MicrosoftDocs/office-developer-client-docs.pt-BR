---
title: Propriedade canônica PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359511"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="955c8-103">Propriedade canônica PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="955c8-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="955c8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="955c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="955c8-105">Contém um valor que indica o tipo de uma linha em uma tabela.</span><span class="sxs-lookup"><span data-stu-id="955c8-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="955c8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="955c8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="955c8-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="955c8-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="955c8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="955c8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="955c8-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="955c8-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="955c8-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="955c8-110">Data type:</span></span>  <br/> |<span data-ttu-id="955c8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="955c8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="955c8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="955c8-112">Area:</span></span>  <br/> |<span data-ttu-id="955c8-113">MAPI não transmitível</span><span class="sxs-lookup"><span data-stu-id="955c8-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="955c8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="955c8-114">Remarks</span></span>

<span data-ttu-id="955c8-115">Essa propriedade aparece somente em tabelas de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="955c8-115">This property appears only on contents tables.</span></span> <span data-ttu-id="955c8-116">Uma categoria só existe quando tem itens.</span><span class="sxs-lookup"><span data-stu-id="955c8-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="955c8-117">Essa propriedade pode ter exatamente um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="955c8-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="955c8-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="955c8-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="955c8-119">Representa dados reais, em vez de uma linha de categoria.</span><span class="sxs-lookup"><span data-stu-id="955c8-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="955c8-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="955c8-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="955c8-121">Não usado no momento.</span><span class="sxs-lookup"><span data-stu-id="955c8-121">Not currently used.</span></span>
    
<span data-ttu-id="955c8-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="955c8-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="955c8-123">A categoria é expandida; normalmente, a interface do usuário exibe isso com o sinal de menos ( - ) ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="955c8-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="955c8-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="955c8-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="955c8-125">A categoria está recolhido; a interface do usuário geralmente exibe isso com o sinal de a mais (+) ao lado dele.</span><span class="sxs-lookup"><span data-stu-id="955c8-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="955c8-126">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="955c8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="955c8-127">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="955c8-127">Protocol specifications</span></span>

<span data-ttu-id="955c8-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="955c8-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="955c8-129">Inclui operações permitidas para os objetos de tabela principais.</span><span class="sxs-lookup"><span data-stu-id="955c8-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="955c8-130">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="955c8-130">Header files</span></span>

<span data-ttu-id="955c8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="955c8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="955c8-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="955c8-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="955c8-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="955c8-133">Mapitags.h</span></span>
  
> <span data-ttu-id="955c8-134">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="955c8-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="955c8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="955c8-135">See also</span></span>



[<span data-ttu-id="955c8-136">Propriedade canônica PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="955c8-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="955c8-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="955c8-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="955c8-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="955c8-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="955c8-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="955c8-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="955c8-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="955c8-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidTagParentDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagParentDisplay
api_type:
- COM
ms.assetid: 6a36f4fb-17c0-4271-87d4-a92895f35f23
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7aef4c1d83672033662502ad0950b7bac9f58c52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429499"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="b4845-103">Propriedade canônica PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="b4845-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="b4845-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4845-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4845-105">Contém o nome de exibição da pasta onde uma mensagem foi encontrada durante uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b4845-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4845-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b4845-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4845-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="b4845-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="b4845-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b4845-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4845-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="b4845-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="b4845-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b4845-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4845-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4845-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b4845-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b4845-112">Area:</span></span>  <br/> |<span data-ttu-id="b4845-113">MAPI não transmitível</span><span class="sxs-lookup"><span data-stu-id="b4845-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4845-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4845-114">Remarks</span></span>

<span data-ttu-id="b4845-115">Essas propriedades não estão em nenhum objeto.</span><span class="sxs-lookup"><span data-stu-id="b4845-115">These properties is not on any object.</span></span> <span data-ttu-id="b4845-116">Eles só podem aparecer no índice de uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b4845-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="b4845-117">Essas propriedades e **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) não estão relacionadas entre si.</span><span class="sxs-lookup"><span data-stu-id="b4845-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="b4845-118">Eles pertencem a contextos totalmente diferentes.</span><span class="sxs-lookup"><span data-stu-id="b4845-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4845-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4845-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b4845-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="b4845-120">Header files</span></span>

<span data-ttu-id="b4845-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4845-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4845-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b4845-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4845-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4845-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b4845-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b4845-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4845-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4845-125">See also</span></span>



[<span data-ttu-id="b4845-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b4845-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4845-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="b4845-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4845-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b4845-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4845-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b4845-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


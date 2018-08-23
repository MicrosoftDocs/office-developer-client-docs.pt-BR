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
ms.openlocfilehash: 910a62a660ea17992aa391d7453919d9fbb53c86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580429"
---
# <a name="pidtagparentdisplay-canonical-property"></a><span data-ttu-id="45c5a-103">Propriedade canônica PidTagParentDisplay</span><span class="sxs-lookup"><span data-stu-id="45c5a-103">PidTagParentDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="45c5a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45c5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45c5a-105">Contém o nome de exibição da pasta onde uma mensagem foi encontrada durante uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="45c5a-105">Contains the display name of the folder where a message was found during a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45c5a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="45c5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45c5a-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="45c5a-107">PR_PARENT_DISPLAY, PR_PARENT_DISPLAY_A, PR_PARENT_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="45c5a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="45c5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45c5a-109">0x0E05</span><span class="sxs-lookup"><span data-stu-id="45c5a-109">0x0E05</span></span>  <br/> |
|<span data-ttu-id="45c5a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="45c5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="45c5a-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="45c5a-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="45c5a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="45c5a-112">Area:</span></span>  <br/> |<span data-ttu-id="45c5a-113">MAPI não transmittable</span><span class="sxs-lookup"><span data-stu-id="45c5a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45c5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c5a-114">Remarks</span></span>

<span data-ttu-id="45c5a-115">Essas propriedades não está em qualquer objeto.</span><span class="sxs-lookup"><span data-stu-id="45c5a-115">These properties is not on any object.</span></span> <span data-ttu-id="45c5a-116">Eles só podem aparecer na tabela de conteúdo de uma pasta de resultados de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="45c5a-116">They can only appear in the contents table of a search-results folder.</span></span>
  
<span data-ttu-id="45c5a-117">Essas propriedades e **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) não estão relacionados entre si.</span><span class="sxs-lookup"><span data-stu-id="45c5a-117">These properties and **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) properties are not related to each other.</span></span> <span data-ttu-id="45c5a-118">Eles pertencem ao contextos completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="45c5a-118">They belong to entirely different contexts.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45c5a-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="45c5a-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="45c5a-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="45c5a-120">Header files</span></span>

<span data-ttu-id="45c5a-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45c5a-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="45c5a-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="45c5a-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="45c5a-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="45c5a-123">Mapitags.h</span></span>
  
> <span data-ttu-id="45c5a-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="45c5a-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45c5a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c5a-125">See also</span></span>



[<span data-ttu-id="45c5a-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="45c5a-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45c5a-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="45c5a-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45c5a-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="45c5a-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45c5a-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="45c5a-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


---
title: Propriedade canônica PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3b4e5fa7228cf243c79a8ec0c9e2b73b7da21c6f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336355"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a><span data-ttu-id="22de7-103">Propriedade canônica PidTagSearchFolderDefinition</span><span class="sxs-lookup"><span data-stu-id="22de7-103">PidTagSearchFolderDefinition Canonical Property</span></span>

  
  
<span data-ttu-id="22de7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22de7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22de7-105">Contém dados que especificam os critérios de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="22de7-105">Contains data that specifies the search criteria.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22de7-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="22de7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22de7-107">PR_WB_SF_DEFINITION</span><span class="sxs-lookup"><span data-stu-id="22de7-107">PR_WB_SF_DEFINITION</span></span>  <br/> |
|<span data-ttu-id="22de7-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="22de7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22de7-109">0x6845</span><span class="sxs-lookup"><span data-stu-id="22de7-109">0x6845</span></span>  <br/> |
|<span data-ttu-id="22de7-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="22de7-110">Data type:</span></span>  <br/> |<span data-ttu-id="22de7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="22de7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="22de7-112">Área:</span><span class="sxs-lookup"><span data-stu-id="22de7-112">Area:</span></span>  <br/> |<span data-ttu-id="22de7-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="22de7-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22de7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="22de7-114">Remarks</span></span>

<span data-ttu-id="22de7-115">O conteúdo específico de cada campo do OBJETO binário grande (BLOB) contido nessa propriedade depende da ID do modelo especificada na propriedade **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="22de7-115">The specific content of each field of the binary large object (BLOB) contained in this property is dependent upon the template ID that is specified in **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)) property.</span></span> <span data-ttu-id="22de7-116">Para obter informações sobre a estrutura BLOB e os modelos de pesquisa, consulte [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="22de7-116">For information about the BLOB structure and search templates, see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="22de7-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="22de7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22de7-118">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="22de7-118">Protocol specifications</span></span>

<span data-ttu-id="22de7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22de7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22de7-120">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="22de7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="22de7-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22de7-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22de7-122">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="22de7-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22de7-123">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="22de7-123">Header files</span></span>

<span data-ttu-id="22de7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22de7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="22de7-125">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="22de7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="22de7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22de7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="22de7-127">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="22de7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22de7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="22de7-128">See also</span></span>



[<span data-ttu-id="22de7-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="22de7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22de7-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="22de7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22de7-131">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="22de7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22de7-132">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="22de7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


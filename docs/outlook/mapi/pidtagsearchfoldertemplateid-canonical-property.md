---
title: Propriedade canônica PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336621"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="90498-103">Propriedade canônica PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="90498-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="90498-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90498-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90498-105">Contém a ID do modelo que está sendo usado para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="90498-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90498-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="90498-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90498-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="90498-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="90498-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="90498-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90498-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="90498-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="90498-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="90498-110">Data type:</span></span>  <br/> |<span data-ttu-id="90498-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90498-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90498-112">Área:</span><span class="sxs-lookup"><span data-stu-id="90498-112">Area:</span></span>  <br/> |<span data-ttu-id="90498-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="90498-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90498-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="90498-114">Remarks</span></span>

<span data-ttu-id="90498-115">Os critérios da pasta de pesquisa são especificados por um modelo.</span><span class="sxs-lookup"><span data-stu-id="90498-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="90498-116">Essa propriedade na mensagem que define a pasta de pesquisa identifica seu modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="90498-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="90498-117">Além de definir critérios de pesquisa, um modelo também define pastas a excluir da pesquisa, define itens a excluir da pesquisa e especifica o valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="90498-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="90498-118">Para obter mais informações sobre modelos de pasta de pesquisa, consulte [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="90498-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="90498-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="90498-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90498-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="90498-120">Protocol specifications</span></span>

<span data-ttu-id="90498-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90498-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90498-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="90498-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90498-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90498-123">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90498-124">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="90498-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90498-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="90498-125">Header files</span></span>

<span data-ttu-id="90498-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90498-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="90498-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="90498-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="90498-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="90498-128">Mapitags.h</span></span>
  
> <span data-ttu-id="90498-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="90498-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90498-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="90498-130">See also</span></span>



[<span data-ttu-id="90498-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="90498-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90498-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="90498-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90498-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="90498-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90498-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="90498-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


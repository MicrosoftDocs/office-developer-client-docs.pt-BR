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
ms.openlocfilehash: 7077210504614d7d95a7f545ea6f37ce02c92fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563244"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a><span data-ttu-id="d097b-103">Propriedade canônica PidTagSearchFolderTemplateId</span><span class="sxs-lookup"><span data-stu-id="d097b-103">PidTagSearchFolderTemplateId Canonical Property</span></span>

  
  
<span data-ttu-id="d097b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d097b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d097b-105">Contém a ID do modelo que está sendo usada para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d097b-105">Contains the ID of the template that is being used for the search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d097b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d097b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d097b-107">PR_WB_SF_TEMPLATE_ID</span><span class="sxs-lookup"><span data-stu-id="d097b-107">PR_WB_SF_TEMPLATE_ID</span></span>  <br/> |
|<span data-ttu-id="d097b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d097b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d097b-109">0x6841</span><span class="sxs-lookup"><span data-stu-id="d097b-109">0x6841</span></span>  <br/> |
|<span data-ttu-id="d097b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d097b-110">Data type:</span></span>  <br/> |<span data-ttu-id="d097b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d097b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d097b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d097b-112">Area:</span></span>  <br/> |<span data-ttu-id="d097b-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="d097b-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d097b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d097b-114">Remarks</span></span>

<span data-ttu-id="d097b-115">Critérios de pasta de pesquisa é especificado por um modelo.</span><span class="sxs-lookup"><span data-stu-id="d097b-115">Search folder criteria is specified by a template.</span></span> <span data-ttu-id="d097b-116">Esta propriedade na mensagem que define a pasta de pesquisa identifica o modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="d097b-116">This property on the message that defines the search folder identifies its corresponding template.</span></span> <span data-ttu-id="d097b-117">Além de definir os critérios de pesquisa, um modelo também define pastas a serem excluídas da pesquisa, define os itens a serem excluídas da pesquisa e especifica o valor do **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d097b-117">In addition to defining search criteria, a template also defines folders to exclude from the search, defines items to exclude from the search, and specifies the value of **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).</span></span>
  
<span data-ttu-id="d097b-118">Para obter mais informações sobre modelos de pasta de pesquisa, consulte [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d097b-118">For more information about Search Folder Templates see [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) .</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d097b-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d097b-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d097b-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d097b-120">Protocol specifications</span></span>

<span data-ttu-id="d097b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d097b-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d097b-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d097b-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d097b-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d097b-123">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d097b-124">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d097b-124">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d097b-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d097b-125">Header files</span></span>

<span data-ttu-id="d097b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d097b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d097b-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d097b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="d097b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d097b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="d097b-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d097b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d097b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d097b-130">See also</span></span>



[<span data-ttu-id="d097b-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d097b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d097b-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d097b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d097b-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d097b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d097b-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d097b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

